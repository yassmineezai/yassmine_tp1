# yassmine_tp1
mon premier projet
YASSMINE EZAI
exercice1:  

ALGORITHMEcode_pin
   Constante_pin=2006:entier
   Variablecode,tentative:entier
DEBUT
   tentative<--3 
   Repeter
     ecrire("Donner le code pin:")
     lire(code)
   si(code=pin)alors
     ecrire("Bienvenue")
   sinon
     tentative<--tentative-1
     ecrire("erreur,code pin est incorrect!!)
   Fin si
    Jusqu'a(code=pin ou tentative=0)
   si(tentative=0)alors
     ecrire(code SIM est bloquee")
   Fin si
FIN

exercice2:

ALGORITHMEechange_valeur
  VARnbr1,nbr2,temp:entier
DEBUT
  ecrire("Donner la valeur du nombre1")
  lire(nbr1)
  ecrire("Donner la valeur du nombre2")
  lire(nbr2)
    temp<--nbr1
    nbr1<--nbr2
    nbr2<--temp
  ecrire("nombre1=",nbr1)
  ecrireln("nombre2=',nbr2)
FIN

exercice3:
ALGORITHMEpgcd_de_deux_nombres
   VARa,b,bgcd,tmp:entier
DEBUT
    ecrire("Donner le premier nombre")
    lire(a)
    ecrire("Donner le deuxieme nombre")
    lire(b)
    pgcd <--a
    Tanque(b!=0)Faire
      tmp<--a
      a<--b
      b<--tmp mod b
      pgcd<--a
    Fin tanque 
    ecrire("le pgcd est:",pgcd)  
FIN 
2)cas de recursivite:

algorithme_pgcd
  VARa,b,bgcd,tmp:entier
   Fonction_pgcd(a:entier,b:entier):entier
   si(b=0)Alors
       retourne a
    sinon
       retourne_pgcd(b,a mod b)
   fin si
   Fin fonction
  DEBUT 
    ecrire("Donner le premier nombre")
   lire(a)
   ecrire("Donner le deuxieme nombre")
   lire(b)
     pgcd<--pgcd(a,b)
    ecrire("le pgcd est :",pgcd)
 FIN   

3)calcul de la complexite:
ALGORITHMEpgcd_de_deux_nombres
   VARa,b,bgcd,tmp:entier
DEBUT
    ecrire("Donner le premier nombre")  1
    lire(a)                             1
    ecrire("Donner le deuxieme nombre")  1
    lire(b)     1
    pgcd <--a   1
    Tanque(b!=0)Faire  log(n)
      tmp<--a
      a<--b
      b<--tmp mod b
      pgcd<--a
    Fin tanque 
    ecrire("le pgcd est:",pgcd)  1
FIN 
-------------------------------------------------
=6+log(n) = log(n)

 pour le cas de recursivite  aussi egal a :log(n)
 on remarque que les 2complexites sont egaux 

 exercice4:
 Algorithme_diviseur_d_un_nombre
   VAR Nombre,b:entier 
procedure afficher_diviseurs (nb:entier)
   VAR b : entier
   b<-1
   pour b de 1 à nb faire
          si (nb mod b  = 0) alors
                     ecrireln (b)
          finsi
   finpour
  fin procedure
Début
 ecrire ("donner le nombre")
 lire (Nombre)
 ecrire("les diviseurs sont :")
	afficher_diviseurs(Nombre)
Fin
 2)
 Algorithme diviseures
    VARi,nombre:entier 
procedure diviseur (nb:entier ) 
    VARi:entier
DEBUT
   pour i de 1 à racine(nombre)	faire
          si (nombre mod i = 0) alors
                        ecrireln(i)
                   si (i != nombre div i) alors
                                   ecrireln (nombre div i)
                   finsi
          finsi
   finpour
   fin
 DEBUT 
      ecrire ("donner le nombre")
      lire (nombre)
      ecrireln ("les diviseur de ",nombre ,"sont")
      diviseur(nombre)
 
Fin
3)

Complexité
methode1
𝑛
O(n)
Méthode 2 (optimisée)	
𝑛	
O(n)

exercice5:

Algorithme SECRET
VAR  nombre_saisir : entier
           reponce : booleen 
CONST  tentative= "5" entier
 Fonction nombre_secret (nb_saisir: entier) : chaine
 VAR   i : entier
              nb_correcte<-alea (1,100)
      fin
           pour i de 1 à tentative faire 
                          si (nb_saisir= nb_correcte) alors
                                             retourne (" félicitations")
                                   si (nb_saisir < nb_correcte) alors
                                                            retourne ("trop petit")
                                                     si (nb_saisir > nb_correcte) alors
                                                                               retourne("trop grand")
                                                     finsi
                                   finsi
                          finsi
                       ecrire ("tentative sont terminer  le nombre correcte est :" aleatoire(1,100))
      fin
Début
tan que (reponce =oui)  faire
ecrire("donner un nombre")
lire (nombre_saisir)
ecrire (tentative(nombre_saisir))
ecrire  ("Voulez-vous réessayer ? ")
                       lire(reponce)
                       fin tan que 
                     
                           finsi
	
Fin 

exercice 6:

Algorithme_Triangle_Floyd
Variables :
    n : entier 
    Procédure AfficherTriangleFloyd(n : entier)
Variables :
    i, j, k : entier

    k ← 1

    Pour i de 1 à n faire
        Pour j de 1 à i faire
            Ecrireln(k, " ")
            k ← k + 1
        FinPour
    
    FinPour

FinProcédure
Début
    Ecrire("Donner le nombre de lignes : ")
    Lire(n)

    AfficherTriangleFloyd(n)

Fin
2)
T(n) : 1+3n+3(n+1)+1+1+1+1+1 = 9 + 6n
 
exercice7: 

Algorithme_SommeBoucle
Variables :
    n, i, Somme : entier

Début
    Ecrire("Donnez un entier n : ")
    Lire(n)

    Somme ← 0

    Pour i de 1 à n faire
        Somme ← Somme + i
    FinPour

    Ecrire("La somme de 1 à ", n, " est = ", Somme)
Fin
2)
Fonction SommeRec(n : entier) : entier
    Si n = 1 alors
        Retourner 1
    Sinon
        Retourner n + SommeRec(n - 1)
    FinSi
Fin

Algorithme TestSommeRec
Variables :
    n : entier

Début
    Ecrire("Donnez un entier n : ")
    Lire(n)
    Ecrire("La somme de 1 à ", n, " est = ", SommeRec(n))
Fin
3) la complexite:
le premier est :𝑂(1)
le deuxieme est :𝑂(n)
