# 100 Days Of Code - Log

### Day 1: January 2nd, 2017

**Today's Progress:** Started (and completed about 90% of) simple app that selects a random set of hex values and sets the background of the container to a gradient of the two values and sets the background of two divs to the first and last of the values. There's a refresh button to select a new set of values.

**Thoughts:** When the page first loads it's blank, so I need to either run the setNewColors function on page load, or provide inital values.

**Link to work:** [Color Generator (though that's not really what it is - I need a better name!)](https://github.com/joshbivens/bgcolorgen)

---

### Day 2: January 3rd, 2017

**Today's Progress:** Added info cards for the seperate color divs and the gradient. I'd say it done.

**Thoughts:** Very simple, but I wanted to figure out how to do this so that I can use it in a bigger app I have planned. Also, using higher order functions is becoming natural to me which is very cool.

**Link to work:** [bgcolorgen](https://github.com/joshbivens/bgcolorgen)

---

### Day 2.5: January 3rd, 2017

**Today's Progress:** Started Tic-Tac-Toe game and it's deceptively complex. Got as far as making the game board and superficially setting the text of the space you clicked on to "X".

**Thoughts:** I need to figure out how the array of subarrays I've set up to house the data for each space relates to the HTML that I return from mapping it to produce the game board.

**Link to work:** [TTT](https://github.com/joshbivens/TTT)

---

### Day 3: January 4th, 2017

**Today's Progress:** Made this convoluted switch function that recieves the added index values of the currently occupied player spaces (checkSpaces checks for "X") and set the text content of a space that would prevent a win to "O", which worked for some of the cases:
```javascript
  ...
  switch (checkSpaces) {
    case 13:
      spaces[4].innerHTML = "O";
      break;
    ...
  }
  ...
```

**Thoughts:** I have the game board mapped to an array, so the top left corner is at index 0, top middle is 1, and so on. Win states occur when three Xs are consecutive (horizontal), skip every 2 spaces (vertical), and skip three spaces (diagonal), so maybe adding their indices wont work in the end. 

I'm all over the place. I need to focus on simplicity and cut the fat.

**Link to work:** [TTT](https://github.com/joshbivens/TTT)

---

### Day 4: January 5th, 2017

**Today's Progress:** Not much. Instead of adding up the total of the indexes of the player moves (and `switch` based on that!), I tried push to a `temp` *array*, but my `switch` didn't respond to cases of, for example, `[1, 2]`, and I'd have pretty much the same result I did when adding them.

**Thoughts:** Arthur Russell is so good... So. There are 3 ways - modes - of winning: vertical, horizontal, and diagonal. Within each mode, there are two ways to complete a set of three: consecutively or alternately. We have to somehow cover all the bases. I'm going to take a break and try something different for the next couple of days.

I just read yesterday's thoughts and I totally forgot about the win states and how they can arise consecutively or *skip* 2 or 3 spaces...hmm.

**Link to work:** [TTT](https://github.com/joshbivens/TTT)

---

### Day 5: January 6th, 2017

**Today's Progress:** Had an idea: The values of the background's linear-gradient's rgb values change depending on how far you've scrolled down. I did this using a template string:

```javascript
  ...
    container.style.background = `linear-gradient(135deg, rgb(${body.scrollTop * 0.01},...)...)`
  ...
```
However, it was really *really* janky. I think it was too much for the repainting process, so I tried just changing opacity and it works smoothly.

**Thoughts:** There has to be way to change a linear-gradient on scroll without some plugin or library. I'll try some more tomorrow.

**Link to work:** [bgchange](https://github.com/joshbivens/bgchange)

---

### Day 6: January 7th, 2017

**Today's Progress:** Made a header that shrinks down on scroll, but that's not all. The body of the document has 4 or 5 sections, 700px each and each with a different color. When you scroll past a section, it's color sticks to the header and becomes a 10px border underneath. Scroll past the next section and it's color becomes a border stacked on the previous one, giving you the impression you're scrolling through a stack of cards.

**Thoughts:** It would be cool to set up some variables (wtih Sass) so that you just indicate the colors of the sections you want beforehand. Right now everything's hard-coded.

**Link to work:** [rainbow-header](https://github.com/joshbivens/rainbow-header)

---

### Day 7: January 8th, 2017

**Today's Progress:** Made a super simple thing where you set the border color of a card from a palette of colors. Made it just to see if I'm at a point where that level of front-end is trivial or not (also I'm sick).

**Thoughts:** It was trivial, which is encouraging.

**Link to work:** [Set Border Color](http://codepen.io/joshbivens/pen/vgNObB)

---

### Day 8: January 9th, 2017

**Today's Progress:** Seeing if making a settings interface will be easy or confusing. It's very early and I have to work soon, *and* I'm sick, so I'll get to more of this tonight or tomorrow.

**Thoughts:** So far, cosmetically, it's been very easy. Now I need to figure out how the settings will actually be presented to the user. This is a programming challenge, but more so a UX/UI challenge.

**Link to work:** [Settings](http://codepen.io/joshbivens/pen/GrppOr/)

---

### Day 9: January 10th, 2017

**Today's Progress:** Work again in a few hours, but I did manage to get a sort of modal window to pop up when you click the settings icon.

**Thoughts:** There's a lot of `position: absolute;`s that might interfere with stuff down the road, but overall I'm happy with today's progress. Tonight or tomorrow, I'll add a few toggles...or maybe a slider that effects the background color! Some setting to top it off.

Update: Added a "Background" setting that let's you set the background color of the "Content". And it works! Pretty cool. Adding more settings, like font style and family, tomorrow.

**Link to work:** [Settings](http://codepen.io/joshbivens/pen/GrppOr/)