+++
title = "Le voyage commence"
date = 2025-10-24
description = "Réflexion sincère sur des entretiens, sur mes lacunes en fondamentaux Rust, et un plan pour réapprendre Rust à travers de courts billets."
tags = ["rust", "learning", "copy-on-write", "career", "reading-plan"]
+++

TL;DR : après un entretien difficile (bonjour `Cow`), j’ai réalisé mes lacunes dans les fondamentaux de Rust. Je reviens aux bases : lire les livres sur Rust de bout en bout et écrire de courts billets sur les concepts clés.

## Le déclencheur

Fin octobre 2025, mon ancienne entreprise, Metagravity, a fermé ses portes. En commençant la recherche d'un nouveau poste, les refus se sont accumulés.
Certaines réponses étaient justifiées : il me manque quelques compétences très demandées (Kubernetes a la cote en ce moment). D’autres ont fait plus mal : mes connaissances en Rust n’étaient pas aussi solides que je le pensais. Un entretien me l’a rappelé crûment. Une question sur `Cow` de Rust ([copy-on-write][cow]) m’a mis sur le grill. Je connaissais le concept, mais je ne l’avais pas encore utilisé en Rust et j’ai peiné sur le problème. Le stress a pris le dessus et j’ai même trébuché sur des bases. Ma confiance fut ébranlée. Après quelques jours de recul, j’y ai vu un signal d’alarme : j’ai eu une belle carrière d’ingénieur logiciel, mais mes fondamentaux Rust doivent être consolidés.

Quand j’ai appris le C, j’ai lu [**The C Programming Language**][1] de Kernighan et Ritchie. Quand j’ai appris le C++, j’ai lu [**C++ How to Program**][2] de Deitel et Deitel. Après 17 ans en tant qu'ingénieur logiciel, j’ai commencé à travailler professionnellement avec Rust en 2023. J’ai commencé à lire [**The Rust Programming Language**][3] et [**l’édition de l'université de Brown**][4], mais je les ai survolés et je me suis mis à coder tout de suite. J’ai appris beaucoup de choses sur le tas, mais je n’ai jamais vraiment pris le temps de solidifier mes connaissances.

## Le remède

J’ai donc décidé de revenir aux fondamentaux. Je vais lire les livres Rust de bout en bout et écrire des billets de blog sur ce que j’apprends. Cela m’aidera à consolider mes bases et à partager mes apprentissages avec d’autres. Je viserai des billets courts, « en petites bouchées », lisibles en moins de 10 minutes, expliquant un concept clé ou une fonctionnalité spécifique de Rust ou de sa bibliothèque standard.

C’est le premier billet de ce parcours. J’espère que vous le trouverez utile.  
Si vous apprenez Rust vous aussi, abonnez‑vous ou laissez un commentaire avec les sujets que vous aimeriez que je couvre.

[cow]: https://doc.rust-lang.org/std/borrow/enum.Cow.html
[1]: https://www.cprogramming.com/books/ritchie.html
[2]: https://deitel.com/c-plus-plus-how-to-program-10-e/
[3]: https://doc.rust-lang.org/stable/book/
[4]: https://rust-book.cs.brown.edu/
