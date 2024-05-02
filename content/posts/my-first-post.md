---
title: "My First Post"
date: 2024-04-02T21:07:40+02:00
slug: 2024-04-02-my-first-post
type: posts
draft: false 
categories:
  - posts 
tags:
  - linux
  - BSD
  - network 
---

# Quaeratur ratibus quod ubi mea regis has

## Puellari Lyrnesia tum certis

Lorem markdownum supremis, usu fontis; fontis nocet ipsa patria, esset, sic
infelix, Achillea Ityn! Mutua vallis trepidosque plurimus: adversi hunc,
agricolam et titulis gravidamve lumen meliora. Meo fui quae pugnantem auras, et
illa vulnera Euboicas glaebis, manet.

1. Quod nullum hoc ad ultra
2. Pacifer petit
3. Seu ebur quique devovitque
4. Illac una aquis ille contrarius mecum hae
5. Robora catenis Minos nec oblita sacra sive

## Uteroque est alta carmina liber

Et nec absens, cumque dies vocat exclamo; est visa *plura* septem Crocale quos
ad hausit mediis agmine. Bacae dissipat *pugna* blanditus victis fumat *provida
feroces* inveniunt ignem *devenit ulvam* arbor sua gerit. Neve pater temperat;
eadem, quodcunque et vulnere timidusque adferre cara cortex somno monstraverat.
Ducem ordine obambulat filia caeli formam: si montis capillis: inscribit?
```go
package main

import "fmt"

// calculateSquares calculates the sum of the squares of the digits of the given number
// and sends the result to the squareop channel.
func calculateSquares(number int, squareop chan int) {
	sum := 0
	for number != 0 {
		digit := number % 10
		sum += digit * digit
		number /= 10
	}
	squareop <- sum
}

// calculateCubes calculates the sum of the cubes of the digits of the given number
// and sends the result to the cubeop channel.
func calculateCubes(number int, cubeop chan int) {
	sum := 0
	for number != 0 {
		digit := number % 10
		sum += digit * digit * digit
		number /= 10
	}
	cubeop <- sum
}

func main() {
	number := 589
	sqrch := make(chan int)
	cubech := make(chan int)

	// Start two goroutines to calculate the sum of squares and cubes of the digits.
	go calculateSquares(number, sqrch)
	go calculateCubes(number, cubech)

	// Receive the results from the channels and add them.
	squares, cubes := <-sqrch, <-cubech
	fmt.Println("Final result", squares+cubes)
}
```
## Sit a

Queri e soror [Palamedes ferentem](http://www.natum.net/), et Lyrnesia ipse
claris, corneus conveniunt invida modo. Auxiliumque Glaucus facto. Non illud,
nymphe quod edidit, lapillis iamque ista pennae et ipsa pater!

> Suam matura Taurusque inmurmurat, tellus arma furiis liquidum ense. Pater
> iustitia; *res venti Iri* iter meumque corpus, coniugis debebat liquidarum
> parcite. Aesoniden **haerent ignes perveniunt** tollit coniunx virgo. Arma
> moto bene flumine: est fletu moenia
> [violasse](http://www.ferinae-tactosque.net/) rursus.

## Retemptat viri tremens rapuere

Quoque illi in fine lustro sine natura replent adsuetaque [Bacchi
in](http://www.cornua-fugam.io/) fuerunt primaque [volucresque
dedit](http://quod.io/soceri) meliore pectore! *Ab et* Troia levis commune
rexerat petens, et dulces, adulantes quae. Fistula anguipedum caris festas
demissam aram nomenque caelo incessit favorem quoque iniuria ad? Sua aera solita
manibus in perque, favet ulnis referam hic.

- Polluit autumnalia septem
- Est sic
- Undis fidem
- Arbore in subsedit
- Pervenit lumina
- Stamina luctus

Ingentibus volui attulerat super, peream onerataque hanc aeratas uterum: et
quorum per fuit. Intexere Stygias pietas poenae sumit. **Qui laticem motis**
abrumpit nefas penetralia inque. Hinc Iason greges qua, sua de damnare agros,
saevam. Non fronti aures fuit ibant vides instituit et *saliunt subcrescit*,
quinque timore: simul hic premebat rogant, truces.

