---
title: "101 Unit Test"
date: 2022-02-21T13:35:52+01:00
draft: false
---





# Pourquoi tester ? tester c'est douter !
https://github.com/mehdyHD/101_unit_test.git

## Type de test:
- tests unitaires : test bas niveau pour tester une seule unité | exécuté en ms
- tests d'intégration : interaction des services (BDD, Api) 
- tests fonctionnels : interagir avec un service selon les exigences métiers
- tests de bout en bout (test automatiques) : reproduire le comportement d'un utilisateur final dans un environnement de test | à automatisé | plusieurs minutes   
- tests d'acceptation : test de PO
- tests de performance : vérifier le comportement en cas de surcharge
- tests de sécurité : OWASP

## Test driven development TDD :
une approche qui consiste à écrire les tests avant la logique métier.

![TDD image](/images/101-unit-test/TDD.JPG)


## le coût des tests :
mike cohn's test pyramid

![test pyramid](/images/101-unit-test/testPyramid.png) 


## Les tests unitaires, pourquoi ? 
-Tester plusieurs scénarios d'un même fonctionnement.
-Factoriser le code.
-Assurer la non regression.

## Caractéristiques
- Fast
- Isolated
- Repeatable
- Self-Checking
- Timely

## Pourquoi on aime pas les tests unitaires ?
- ça demande une certaine rigueur.
- ça prend du temps (on oublie de les estimer) 
- l'architecture du code ne facilite pas l'écriture des tests (Interface, static )
- Il faut les maintenir à jour.

## Couverture de code 
### pourquoi ? 
- une indication quantifiable sur le degré de test.
ça aide a créer plus de scénarios de tests.

### comment je fais pour le calculer ? 
- Via visual studio
- Via sonar cloud

== Une bonne couverture ne veut pas dire que le code est bien testé == mais ça n'empêche pas de l'avoir dans les conditions de PR

## Mocker
### quoi ?
simuler le comportement d'un objet.
### pourquoi ?
pouvoir définir un résultat attendu pour un objet (pas de contrainte BDD , API ...)

## Architecture N-Layer
![Nlayer image](/images/101-unit-test/nlayer.JPG)


## Test unitaire à la Cegid pour Acumatica
- 80% couverture de code.
- user interface piloter par le code | architecture.
- MsTest | Moq | Fixiture
- exemple : BatchReleaseExtTests , APReleaseProcessYearClosingTests , POOrderEntryExtTests 


## Bonne pratiques 
(https://docs.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices)
- Naming your tests
- Arranging your tests
- Write minimally passing tests
- Avoid magic strings
- Avoid logic in tests
- Avoid multiple acts




















