# Navigation Bar Across Top of Screen


### Step 1: Setting up the files

To start, create four files: ```index.html``` ```page1.html``` ```page2.html``` ```style.css```

Next, open the ```index.html``` file. First, we will declare a doctype. We’re using html as our coding language, so we will type ```<!DOCTYPE HTML>```. 

Now, we will create the shell of the webpage. Start with the ```<html>``` tag. Inside the html tag, put a ```<head>``` tag and a ```<body>``` tag. Your file should look like this: 

```html
<!DOCTYPE HTML>
<html>
	<head></head>
	<body></body>
</html>
```

### Step 2: Creating the navbar

In the body, create a ```<nav>``` tag. Inside the tag, create an ```<a>``` tag. Inside the tag, type ```Home```. Create two more ```<a>``` tags, for Page 1 and Page 2. 

Now add some text to the page in a div. After the ```</nav>``` tag, but still in the body add a ```<div>``` tag. Inside the tag, add whatever text you want. Your file should now look something similar to this:

```html
<!DOCTYPE HTML>
<html>
    <head></head>
    <body>
        <nav>
            <a>Home</a>
            <a>Page 1</a>
            <a>Page 2</a>
        </nav>
        <div>
            Home is where the wifi is.
        </div>
    </body>
</html>
```

### Step 3: Linking to the other pages

In order to link the other pages, we will have to go inside the ```<a>``` tag. Right after the a of the first tag, press the space bar, then type ```href=”index.html”```. Do the same for ```page1.html``` and ```page2.html``` in their respective tags. The three should now look like this:

```html
<a href="index.html">Home</a>
<a href="page1.html">Page 1</a>
<a href="page2.html">Page 2</a>
```

Now open the other two html files and do a little copy paste of the ```index.html``` document into them. Then, change the text in the div so that each page displays unique text. Hit run. Go to preview > Live Running Preview. The buttons should now work

### Step 4: Styling the navbar

Although your navbar is working, it’s pretty ugly. It’s time for some css styling. In the head of the index.html file (we will work on the index, then do another copy paste to the pages at the end), we’re going to link the css file. Type <link href="style.css" rel="stylesheet"> in the head. 
Next, open the css file.
First, we’re going to get rid of the automatic page margin. Type ```body {```, then click enter and in the parentheses type ```padding:0px```; and on the next line, ```margin: 0px;```.

Second, we’re going to style the navbar. Type ```nav {``` and inside, type ```background-color: #4090C0;``` ```width:100%;``` and ```padding: 10px;``` The background color uses hexadecimal (base-16) values (40 red, 90 green, C0 blue) to represent hues, the width at 100% makes the navbar as wide as the page is wide, and the padding gives the elements inside 10 pixels of space from them to the edge of the page.

The current state of the ```style.css``` should be:

```css
body {
    padding:0px;
    margin: 0px;
}
nav {
    background-color: #49C;
    width:100%;
    padding: 10px;
}
```

Now, we will switch back to the html file.

The ```<a>``` tags need a name to be called by in the css file to add styling to them, without messing with other a tags that could exist on a page (```<a>``` tags are often used for hyperlinks). We will be using classes. A class is very similar to a Facebook group. Each a tag that wants to join will need to apply for membership, so to speak. Let's code this.

Inside the ```<a>``` tag, next to where we previously put the ```href```, we will type ```class=”navButton”```. This allows all of our a tags to join the ```.navButton``` class. 

The updated ```<a>``` tags should look like this:

```html
<a class="navbutton" href="index.html">Home</a>
<a class="navbutton" href="page1.html">Page 1</a>
<a class="navbutton" href="page2.html">Page 2</a>
```

In the css, we will now style the entire ```.navButton class```. 

Type ```.navButton {```, then click enter and in the parentheses type ```font-size: 30px;``` ```font-family: Arial;``` ```padding: 25px;``` ```color:#336;``` ```text-decoration: none;```. The removal of text decoration gets rid of the underline, as well as other automatic styling of ```<a>``` tags. 

The update to the ```style.css``` should look like this:

```css
.navbutton {
    font-size: 30px;
    font-family: Arial;
    padding: 25px;
    color:#336;
    text-decoration: none;
}
```

### Step 5: Congratulations!

You’ve made it! Try to think of ways you can style this further. For example, maybe style the text the same way we did the ```<a>``` tags. If you don’t know how to do something, don’t hesitate to ask any one of us for help. 
