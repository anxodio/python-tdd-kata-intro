# TDD Katas

## An introductory Python workshop

---

## What is software testing

---

> Software testing is the act of examining the artifacts and the behavior of the software under test by validation and verification

_Wikipedia definition_

Note:
Pot semblar complexe, però simplificant artifact és el output d'una peça de software
(en python pot ser dificil d'entendre), i el SUT es el que estem provant (paraula tipica)
Al final busca comprovar requeriments, descobrir bugs, etc

Amb el public, se us acuden exemples? beta testing per exemple ho coneix quasi tothom

---

You can test software manually, but also it can be

### ✨🌈 automated 🌈✨

---

### Types of automated tests

- Unit tests
- Integration tests
- End to end tests
- And more (functional, acceptance, performance, ui...)

Note:
Explicar que ens centrarem sobretot en els unit test

---

### Types of automated tests

![Testing pyramid](img/pyramid.png)

Note:
Passar per sobre per explicar la importancia dels unit test com a fonaments

---

## Testing in Python

---

### A simple Python test example

```python
def add_one(x: int) -> int:
    return x + 1
```

```python
def test_add_one() -> None:
    assert add_one(-1) == 0
    assert add_one(7) == 8
```

<!-- .element: class="fragment fade-in" -->

Note:
Aprofitar per explicar type hinting com a forma extra de validar el nostre software
Explicar que hi ha varies formes de testejar en python, aqui simplifiquem a pytest

---

### How executing tests looks like


![Example OK test output](img/test_ok.png)

---

### How executing tests looks like


![Example failing tests output](img/test_fail.png)


---

## Test Driven Development (TDD)

---

> TDD is a **software development process** relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. This is as **opposed to software being developed first and test cases created later**.

_Wikipedia definition_

Note:
Massa llarg, demanem al public centrarse en la negreta: proces, metode, test abans
Es podria entrar més en detall (detroit o london per exemple), pero no es el moment

---

### Three Rules of TDD

1. Write production code only to pass a failing unit test.
2. Write no more of a unit test than sufficient to fail (compilation failures are failures).
3. Write no more production code than necessary to pass the one failing unit test.

---

### Red Green Refactor

![Red green refactor diagram](img/red_green_refactor.jpg)

---

### TDD Example

```python
def test_add_two_numbers() -> None:
    assert add_two_numbers(1, 2) == 3
    assert add_two_numbers(-5, 5) == 0
```

NameError: name 'add_two_numbers' is not defined

<!-- .element: style="color: red" class="fragment fade-in" -->

---

### TDD Example

```python
def add_two_numbers(x: int, y: int) -> int:
    return x + y

def test_add_two_numbers() -> None:
    assert add_two_numbers(1, 2) == 3
    assert add_two_numbers(-5, 5) == 0
```

Test OK

<!-- .element: style="color: green" class="fragment fade-in" -->

---

## What is a Kata

TODO
A code kata in programming is an exercise aimed at programmers developing their skills through practice and repetition.

---

## THE KATA

---

# ¡Gracias!
