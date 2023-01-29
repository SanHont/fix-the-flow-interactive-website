# Interactie voor de opdrachtgever

## De opdracht beschrijving
Het doel is om een website te maken voor de partners van Vervoerregio Amsterdam om te laten zien wat je moet doen om de desbetreffende website toegankelijk te maken. De toegankelijkheid wordt een groot probleem als mensen met een beperking websites proberen te bezoeken maar deze niet goed toegankelijk zijn. Vervoerregio Amsterdam wil kunnen laten zien aan partners wat zij moeten doen om hun website toegankelijker te maken. 

En deze website mochten wij voor hun maken, de interactie die ik heb gekozen was om een contact formulier te maken, via dit formulier kan de gebruiker gemakkelijk contact opnemen met de ontwikkelaar. En ik heb dit zo gemaakt dat als je op een knop drukt dat dan het formulier verschijnt.

## Code voorbeelden
```html
        <button type="button" class="display-vragen-formulier">
            <p>Verstuur een bericht</p>
        </button>

        <div class="vragen-formulier">
            <form>

                <label for="fname">Voornaam *</label>
                <input type="text" id="fname" name="firstname" placeholder="Uw voornaam" required>

                <label for="lname">Achternaam *</label>
                <input type="text" id="lname" name="lastname" placeholder="Uw achternaam" required>

                <label for="lname">E-mail *</label>
                <input type="text" id="lname" name="lastname" placeholder="info@vervoerregio.nl" required>

                <label for="subject">Onderwerp *</label>
                <textarea id="subject" name="subject" placeholder="Bereik ons met al uw vragen." required></textarea>

                <input type="submit" value="Verzenden">
            </form>
        </div>
```
Hier is de html te zien waarin ik dus de button heb staan en ook het formulier. 

```css
.display-vragen-formulier {
    border: 1px solid var(--licht-grijs);
    font-family: 'Fira Sans Regular';
    background-color: var(--wit);
    border-radius: 4px;
    font-size: 1.2rem;
    height: 2.4rem;
    z-index: 0;
    width: 14%;
}

.undisplay-vragen-formulier {
    z-index: -1;
}

.display-vragen-formulier:hover {
    border: 1px solid var(--licht-grijs);
    background-color: var(--licht-grijs);
}

.vragen-formulier {
    transition: transform 0.5s ease-out;
    background-color: var(--wit);
    transform: translateX(200%);
    border-radius: 5px;
    max-width: 20rem;
    padding: 20px;
}

.vragen-formulier-display {
    transform: translateX(-200px);
}

@media (max-width: 800px) {
    .vragen-formulier-display {
        transform: translateX(0px);
    }
}
```
Hier is de CSS waarin je kunt zien hoe ik de button en het formulier heb gestyled, en ook hoe ik het formulier onzichtbaar maak door het buiten het scherm te zetten.

```js
let contactForm = document.querySelector(".vragen-formulier")
let buttonForm = document.querySelector(".display-vragen-formulier")
console.log(buttonForm)

buttonForm.addEventListener('click', displayForm)

function displayForm() {
    contactForm.classList.add('vragen-formulier-display')
    buttonForm.classList.add('undisplay-vragen-formulier')
}
```
Met de JavaScript zorg ik er voor dat wanneer je op de button klikt het formulier wel weer zichtbaar wordt door een andere class te togglen waarbij het formulier binnen het scherm wordt geslepen.

## De website nu
De website is live te zien op: http://sanhont-vervoerregioamsterdam.student.fdnd.nl/

En hier zijn 2 foto's van de website als het formulier er niet is en wanneer het er wel is.

<img src="https://user-images.githubusercontent.com/112860052/215324611-e425f9b0-ef68-434d-83fe-3186e2dce839.png" width="70%">
<img src="https://user-images.githubusercontent.com/112860052/215324685-87037df1-db58-40b2-9c5d-a8ffb4e96565.png" width="70%">
