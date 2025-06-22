---

class: center, middle

## \#SmooshGate

---

class: center, middle, big

`array.flatten()`

---

class: center, middle, big

![Firefox Nightly](firefox-nightly.png)

---

class: center, middle, huge

😞

---

class: center, middle

![Mootools](mootools.png)

---

???

Around 2018, a new method got added to JavaScript arrays: `Array.flat()`

What flat does is not particularly important for this story, but it operates
on an array of arrays, and concatenates them into a single array.

When the method was originally proposed, it was called `flatten`. After all,
that's what most other languages call it. `flatten` is a verb, and `flat` is not.
So why did the name change?

The problem was, a popular library called MooTools had already added their own
`flatten` method to arrays, but they did it in a way that subtly depended on the
method _not_ existing as a built-in JS feature. So when the built-in flatten method
shipped to Firefox Nightly, existing websites that used MooTools stopped working
in that browser.

Now, to be clear, patching new behavior onto built-in language features like MooTools
was doing is NOT a good practice, and SmooshGate exemplifies why.

So, what do you think the web standards people did?

---

class: small

## Choose your own adventure

<div class="letter-list-next"></div>

1. Release `flatten()` as-is, and break websites using MooTools.

--

2. Contact the MooTools developers and get them to fix their code.

--

3. Contact the website maintainers and get them to stop using MooTools.

--

4. Change the `flatten()` proposal to be compatible with MooTools and existing websites.

--

5. Give up, retire to the country, and start a pigeon-training business.


---

class: center, middle, big

`array.flat()`
