# Dengue-Cubano

   git clone https://github.com/Carlos496/Dengue-Cubano.git
   cd Dengue-Cubano 
   
% Las Reglas
gripe(X):- malestar(X), fiebre(X), tos(X),sec_nas(X).
dengue(X):- malestar(X), fiebre(X), dolor_art_mus(X), rash(X).
El diagnóstico 
diagnostico(X):-nl, write('Se investiga GRIPE'),gripe(X),
             nl, write(X), write(' tiene sintomas de GRIPE.'),fail.
diagnostico(X):-nl, write('Se investiga DENGUE'), dengue(X),
             nl, write(X),write(' tiene sospecha de DENGUE.').
diagnostico(X):-write(' NO SE LOGRO UN DIAGNOSTICO.').
Consulta 1
?- diagnostico(pepe).
Se investiga GRIPE
pepe tiene malestar? [s/n]: s.
pepe tiene fiebre? [s/n]: |: s.
pepe tiene tos? [s/n]: |: n.

Se investiga DENGUE
pepe tiene malestar? [s/n]: |: s.
pepe tiene fiebre? [s/n]: |: s.
pepe tiene dolor muscular o en articulaciones?[s/n]: |: s.
pepe tiene rash [s/n]: |: s.
pepe tiene sospecha de DENGUE.
Consulta 2
?- diagnostico(pepe).
Se investiga GRIPE
pepe tiene malestar? [s/n]: s.
pepe tiene fiebre? [s/n]: |: n.

Se investiga DENGUE
pepe tiene malestar? [s/n]: |: s.
pepe tiene fiebre? [s/n]: |: n.
 
NO SE LOGRO UN DIAGNOSTICO.

    git add diagnostico_dengue.pl
git commit -m "Agregar programa de diagnóstico del dengue"
git push origin master

git checkout -b mejoras
git add diagnostico_dengue.pl
git commit -m "Agregar mejoras al diagnóstico"
git push origin mejoras

git checkout -b pruebas 
git add diagnostico_dengue.pl
git commit -m "Agregar pruebas al diagnóstico"
git push origin pruebas

git branch -a



