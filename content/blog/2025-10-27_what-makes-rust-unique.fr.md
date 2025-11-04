+++
title = "Ce qui rend Rust unique"
date = 2025-11-04
+++

Chaque langage a ses atouts et ses particularités ; Rust se distingue en offrant à la fois performance et sécurité !
Le compilateur, à la fois allié et exigeant, impose la propriété (ownership) et l’emprunt (borrowing) à la compilation ; vous obtenez ainsi la sûreté mémoire sans ramasse-miettes (garbage collector).

Déballons tout ça en moins 5 minutes.

---

## Propriété (Ownership)

En Rust, chaque valeur a exactement un propriétaire. Quand ce propriétaire sort de portée (scope), la valeur est automatiquement détruite.

```rust
{ 
    let s = String::from("Hello");
    // s est valide ici
} // s sort de portée -> la mémoire est libérée
```

Pas de `free()`, pas de GC. Juste un nettoyage automatique.

---

## Mouvements (Moves) et copies

Quand vous assignez ou passez des valeurs, la propriété est généralement déplacée (move), pas copiée :

```rust
let a = String::from("hi");
let b = a; // a est déplacé dans b
// println!("{}", a); ❌ erreur : emprunt d'une valeur déplacée : `a`
```

Pour les types `Copy` (principalement les types primitifs), Rust les duplique silencieusement au lieu de les déplacer.
On peut voir cela comme « peu coûteux à copier » vs « doit être déplacé ».

---

## Emprunt (Borrowing)

Au lieu de transférer la propriété, vous pouvez emprunter des données :

```rust
fn greet(name: &String) {
    println!("Bonjour, {name} !");
}

let s = String::from("Alice");
greet(&s); // on emprunte s, on ne le déplace pas
println!("{}", s); // s est toujours valide
```

Les références permettent de lire ou de modifier des données temporairement, tandis que le compilateur garantit que vous ne créez pas d’accès mutable conflictuels.
C’est le borrow checker qui fait son travail.

---

## L’idée majeure

Rust impose, à la compilation, qui possède quoi et combien de temps une valeur vit.
Cela rend les data races, les use-after-free et les pointeurs pendants impossibles en Rust sûr.

C’est strict, parfois frustrant, mais une fois le modèle intégré, on en perçoit l’élégance.

---

La prochaine fois : nous réimplémenterons `Option<T>` à partir de zéro et verrons comment les enums propulsent une bonne partie de la bibliothèque standard de Rust !
