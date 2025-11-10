## What is HTML?

HTML stands for `HyperText Markup Language.`
It's code that defines the structure and content of a webpage.

HTML is made up of elements. The first one we will use is the `h1` element:

```html
<h1>Welcome to freeCodeCamp</h1>
```

It starts with an opening tag (`<h1>`), ends with a closing tag (`</h1>`), and has the text it will display in between the tags.

An `h1` element is the main heading of a webpage and you should only use one per page.
`h2` elements represent subheadings. You can have multiple per page and they look like this

```html 
<h2>This is a subheading.</h2>
```

When you need to add a paragraph to a webpage, you can use the `p` element like this:

```html 
<p>This is a paragraph element.</p>
```

There are six heading elements in HTML:`h1` through `h6`.They're used to show the importance of sections of your webpage, with `h1` being the most important and `h6` the least.

## What Role Does HTML Play on the Web?

HTML, which stands for Hypertext Markup Language, is a markup language for creating web pages. When you visit a website and see content like paragraphs, headings, links, images, and videos; that's HTML.

Here is a small example using HTML elements. Try editing some of the text in the editor and see the changes update in the preview window.

```html
<h1>Main heading element</h1>

<p>I am a paragraph element.</p>
```

HTML represents the content and structure of a webpage through the use of elements. Most elements will have an opening tag and a closing tag. Sometimes those tags are referred to as start and end tags. In between those two tags, you will have the content. This content can be text or other HTML elements.

Both opening and closing tags start with a left angle bracket (`<`), and end with a right angle bracket (`>`), with the tag name placed between these angle brackets. While HTML tag names are case-insensitive, it is a widely accepted convention and best practice to write them in lowercase.

Here is a closer look at just the opening and closing paragraph tags:

```html
<p>
  
</p>
```

What distinguishes an opening tag from a closing tag is the forward slash (`/`) placed immediately after the left angle bracket in a closing tag. Some HTML elements do not have a closing tag. These are known as void elements.

Here is an example of an image element which is a void element:

```html 
<img>
```

Notice that this image element does not have the closing tag and it does not have any content. Void elements cannot have any content and only have a start tag.

Sometimes you will see void elements that use a `/` before the `>` like this:

```html
<img />
```

While many code formatters like Prettier, will choose to include the `/` in void elements, the HTML spec states that the presence of the `/` "does not mark the start tag as self-closing but instead is unnecessary and has no effect of any kind".

In real world development, you will see both forms so it is important to be familiar with both.

If you wanted to display an image, you will need to include a couple of attributes inside your image element. An attribute is a special value used to adjust the behavior for an HTML element.

Here is an example of an image element with a `src` attribute. Update the value of the `src` attribute to `https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg` and you will see the image change to two cats peacefully sleeping.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" />
```

The `src` attribute is used to specify the location for that image. For image elements, it's good practice to include another attribute called the `alt` attribute. The alt attribute is used to provide short, descriptive text for the images.

Here's an example of an image element with the `src` and `alt` attributes. Try breaking the image by updating the `src` value to `"https://.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"`. You will see the image disappear and only the `alt` text show.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />
```

## What Are Attributes, and How Do They Work?

An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additional information about the element or specify how the element should behave. Here is the basic syntax for an attribute:

```text
<element attribute="value">

</element>
```

The attribute name is followed by an equal sign (`=`) and a value in quotes. The value can be a string or a number, depending on the attribute.

This first example uses the `href` and `target` attributes. The `href` attribute specifies the URL of a link and the `target` attribute specifies where to open the link.

Change the `href="https://www.freecodecamp.org/news/"` to `href="https://www.freecodecamp.org"`. Now when you click on the link in the interactive editor, you will see the freeCodeCamp homepage in a new browser tab.

```html
<a href="https://www.freecodecamp.org/news/" target="_blank">
  Visit freeCodeCamp
</a>
```

Without the `href` attribute, the link would not work because there would be no destination URL. So you must include this `href` attribute to make the link functional. The `target="_blank"` enables the link to open in a new browser tab. You will learn more about the `target` attribute in future lessons.

Other common attributes are the `src`, and `alt`, or alternative, attribute - which is used to specify the source of an image and provide alternative descriptive text for the image, respectively.

Change the `src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"` to s`rc="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg"`. Then change the `alt="Two tabby kittens sleeping together on a couch."` to `alt="Two cats running in the dirt."`.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />
```

Similar to the `href` attribute, the `src` attribute is required because it specifies the image file to be displayed. The `alt` attribute is not required, but it is recommended for accessibility purposes. Accessibility means making sure that everyone, including those with disabilities, can use and understand things like websites, apps, and physical spaces. You will learn more about accessibility in the upcoming lessons.

Some attributes are a little unique with their syntax like the `checked` attribute.

Try clicking on the checkbox in the preview window to see it alternate between a checked and unchecked state.

```html
<input type="checkbox" checked />
```

In the following example, we have an `input` element with the `type` attribute set to `checkbox`. Inputs are used to collect data from users, and the `type` attribute specifies the type of input. In this case, this input is a checkbox. You will learn more about how inputs work in the upcoming lessons.

The `checked` attribute is used to specify that the checkbox should be checked by default. The `checked` attribute does not require a value. If it is present, the checkbox will be checked by default. If the attribute is not present, the checkbox will be unchecked. This is known as a boolean attribute. You will learn more about booleans in general when you get to the JavaScript section.

Remove the `checked` attribute from the `input` in the interactive editor, and you will see that the checkbox is no longer checked by default.

```html
<input type="checkbox" checked />
```

There are several common boolean attributes you will encounter in HTML, such as disabled, readonly, and required. These attributes are used to specify the state of an element, such as whether it is `disabled`, `read-only`, or `required`.

Here is an example of a text `input` element that is disabled by default. Try clicking on the `input` element in the preview window. Now remove the `disabled` attribute from the `input` element and you will see that the `input` is no longer disabled by default. You should now be able to click on it and type inside the field.

```html
<input type="text" disabled>
```

HTML has many attributes that can be used to customize the behavior and appearance of elements on a webpage. Understanding how to use attributes is essential for creating interactive and accessible web content. Over the next few lessons, you will learn about more HTML attributes and how to use them effectively in your web development projects.