W ramach zadania skonfigurowano workflow GitHub Actions do budowania wieloarchitekturowego obrazu Dockera, jego publikacji na DockerHub oraz przeprowadzenia testu na obecność podatności.

![alt text](https://github.com/lukaszlikos/zadanie_2/blob/master/images/buildx.png)
Do przeprowadzenia testu wykorzystano narzędzie Docker Scout 

tryb skanowania cves
wyswietlenie podsumowania
kod błędu w przypadku wykrycia zagrożeń HIGH lub CRITICAL
![alt text](https://github.com/lukaszlikos/zadanie_2/blob/master/images/Zrzut%20ekranu%202024-12-15%20024947.png)

Wstępnie przeprowadzono test działania bez wywołania kodu błędu w celu poprawności działania workflow, kolejno dodano parametr exit-code: "1"
i ponownie zwerfikowano działanie. 

![alt text](https://github.com/lukaszlikos/zadanie_2/blob/master/images/Scout%202.png)
![alt text](https://github.com/lukaszlikos/zadanie_2/blob/master/images/Scout.png)

Dodatkowo w repozytoriu załączono logi z działania workflow.
