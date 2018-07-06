---
title: HTML Accessibility. Get Started Now !  
comments: true  
---  
  
Providing the user a good way to navigate and interact with your site. Make your HTML code as semantic as possible, so that the code is easy to understand for visitors and screen readers.
  
  
Making an HTML semantic is a helpful way to give a user an easy way to navigate to your website and interact more with it. The code will be readable and understandable for the users.

  
* **Get Started!**  

When I started developing my first web page, My only concern was to get the content online. I didn’t focus on the usability, functionality, performance, accessibility, and UX.
 
 
 Later on, I have discovered that some web pages are loading faster than mine. My web page was too slow, and I wanted to make it at least a similar speed compare to other web pages, So I start reading more and more about HTML, critical CSS, speed indices font loading etc.
 
 After so many tries and research I could reach a good level of knowledge and focus more on the responsiveness of the website. I started focusing on the HTML accessibility because it is the foundation of what we begin with as a web developer.
 
 
 In this post, I will be giving some tips and examples that need to keep in mind for accessibility tips.
 
 
 * **lang [set the HTML language]**  

By defining the language on your document that will make it easy for the browser that which language you are using and its good in in terms of SEO.


For Example 

```
<html lang="en"> 
   .......
   .......
   </html>
``` 
  
Also using the **lang** attribute will help you to switch between languages on specific attributes like:
  

```$xslt
 <p> hello world <i lang=“ar”> this is an Arabic language </li> </p>


```

You need to make sure to use the correct term of the language.


 
  
* **hidden [using a hidden attribute]**  
  
  
Using a hidden attribute in **CSS** to hide the content from the reader if you want!.

```
[hidden] {
display: none;
}
 ``` 
 
But this attribute will not work with IE10 and lower .

  
  
  
* **alt [adding alt attribute to the img tags]**  
  
  
 Using the **alt** attribute in the image will give a good description of it and will help the SEO especially when its added as content.  
 
 
 you can leave the **alt** attribute empty or add addiction of the image.

  
  If the image is purely decorative or doesn’t add valuable information, consider embedding it with CSS as a background image. If you have/want to add it in HTML, don’t remove the **alt** attribute, but leave it empty.

  
  
```$xslt
<img src="1_image.jpg" alt="book"/>

```
 
 
 
Because deleting the attribute indicates that the image is a key part of the content, and no textual equivalent is available.

So by setting this attribute to an empty string that indicates the image is not a key part of the content and that non-visual browsers may delete it from rendering.


 
 * **button [you need a button ? then use a button]**

If you need to create a button in html you can use `<button >` Tag and do not use `<p>` tag.


```$xslt
<button>Click here</button> <p>Click here</p>

```

**why should we use the button element?**

Using the button elements is good for

1. **focusable**
  
2. **Screen readers identify them as buttons**
  
3. **Clickable**
  


**H1 [use a crochet heading]**

using a heading tags `<h1>-<h6>` helps the user to have a better understanding of the structure of the page and the relationship between individual structures. 


 By using the [**tota11**](http://khan.github.io/tota11y/) it will help to check the page outline.



**Go Beyond**

These were some of the tips that can help to write accessible HTML. There are more and more tips that can be found in other resources.


[HTML: A good basis for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)

[Accessibility and HTML](https://www.codecademy.com/articles/accessibility)