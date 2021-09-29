# Create your own Storyline
## In this document you will find all the basics you need to know when creating your own story

---
---

### Basics
So, the fundamental knowledge is:
- You need to know HTML, [CSS](#css-knowledge) and [JavaScript](#javascript-knowledge)
- You need to know [how storyline is constructed](#storyline-construction).

### [JavaScript](https://developer.mozilla.org/docs/Web/JavaScript) Knowledge
- [DOM](https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction)
- [LocalStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage)
- [Functions](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Functions)
- [Variables](https://developer.mozilla.org/docs/Learn/JavaScript/First_steps/Variables)
###### Sources: [Moz://a Developer](https://developer.mozilla.org)

### [CSS](https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web/CSS_basics) Knowledge
- As in HTML, just to be able to style, but not styling such as `<b>`, `<i>`, `<u>`, but the CSS like.
  Example:
```css
tag {
  style: style;
 }

.class {
  style: style;
}

#id {
  style: style;
}
```

### [HTML](https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web/HTML_basics) Knowledge
- Just a basic knowledge, such as `<b>`, `<i>`, `<u>` etc. Just to be able to style the text, and not to write the whole page.

### Storyline Construction
So the storyline is written is JavaScript file `(.js)`. The example can be the main storyline which comes with game. Let's look in the demo's version code.
```js
function sc1() {
    localStorage["us"] = "1";
    return ngs();
}
function sc2() {
    localStorage["us"] = "2";
    return ngs();
}
function sc3() {
    localStorage["us"] = "3";
    return ngs();
}

function ngs() {
    var nickname = localStorage["nickname"];
    var cm = localStorage["cm"];
    var us = localStorage["us"];
    var ne = document.createElement("p");
    var sc = document.getElementById("divStoryContent");
    if (cm == "1") {
        localStorage["cm"] = "2";
        ne.innerHTML = `
        <i>Another day... I want to go back to home and forget about all this mess... <br>
        Why me? I think I should end my suffering... But still, I need to go to school anyway.
        <br><br>
        I'm right in front of the class door, and I'm late. It won't end good... </i>
        <br>
        <br>
        - Good morning, I'm sorry, I'm late. <br>
        - Yes, I see, sit down. <br>
        <i>Thankfully She didn't complained. </i>
        <br>
        <br>
        <br>
        <p style="font-size: 1.5vw;">&nbsp&nbsp <b>Hour later... </b></p>
        <br>
        <br>
        <i>Oh God, it's only the first hour and I am done...</i> *sits in the corner* <br>
        - ` + nickname + `? What are you doing? <br>
        - Nothing, leave me alone... <br>
        - NO! I don't just leave you because you said so. What's wrong? <br>
        - <i>Sight</i> We'll talk about it later... Okay? <br>
        - Ugh... Okay. <br>
        <i>And that's how I've got additional hours of another suffer... GREAT.</i>
        <br>
        <br>
        <br>
        <br>
        <p style="font-size: 2.5vw;">Thank you for downloading the Demo version. Please come back when the full version will get released!</p>
        `;
        sc.appendChild(ne);
    };
}
```
As you can see, there are two functions in the beggining. Those takes responsibility for handling player's choices.
```js
function sc1() {
  localStorage["us"] = "1";
}
```
`sc1()` is just shorten `selected choice 1`.
`localStorage["us"] = "1";` this is responsible to contain user's decission. `["us"]` stands for `user select` and `= "1";` is saving the decission as the first one. You can default set only 3 decissions at one time, but you can create more, if you need to.
