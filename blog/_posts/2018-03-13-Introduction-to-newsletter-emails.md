---
title: Introduction to newsletter emails  
comments: true  
---  
  
Nowadays the email newsletter is taking a good advantages of marketing strategies. But it's not all about generating a random newsletters that will bring you a better conversion.  
There are some techniques and steps need to be followed in order to make a better newsletter.  
  
In my first blog post i will be talking from the technical side on how we can create or structure a Newsletter email and what are the things we need to consider while building those templates and how it will be  tested before we send it to the subscribers.  
  
* **Email clients**  

First of all we need to be aware that each email client like  (_Gmail 
, Yahoo, Outlook, Mail, etc_)  does not accept all the CSS properties and sometimes it will override it with it's own CSS. So we need to use sometimes an `!important` attribute. It means that
> this is important, ignore subsequent rules, and any usual specificity issues, apply this rule!. 
 
For Example 

```html 
<span style="color:red !important;">hello world</span>
``` 
  
Remember that some email clients will automatically transform typed out hyperlinks into links (if we don't anchor `<a>` them ourselves). This can sometimes achieve negative effects (say if we're putting a style on each of the hyperlinks to appear a different color).  
  

  
* **In-line CSS**  
  
  
When we start developing a newsletter template we need to write an **Inline CSS** for the most **HTML** Tags. For an Example: 
 
 ```html 
 <p style="color: red;">Hello World</p>  
 ``` 
 
 Because those Email clients won't reference external CSS files, because it might interfere with their own CSS coding. We recommend placing your CSS code in-line with your content instead of using body and head tags  
  
  
  
* **Tables or Divs?**  
  
  
  
Start using `<table>` instead of `<div>` tags to control our design layout and the structure of the newsletter email.  
  
When it comes to email **HTML**, note that all best practices from Web development goes out the window. We Should use Tablets instead of Divs. Because **HTML** Tables are likewise supported by every major email client.  
  
So, if we want the email newsletter to display relatively well across email clients we need to use **HTML** tables to lay out our newsletter campaigns.  
  
below it shows what **HTML** tags we can use in building the newsletter email.  
  
  
 
  
  
  | Instead of this | Use this |
  | --- | --- |
  | `<div>` | `<table>, <tr>, <td>` |
  | `<p>` | `<td>` |
  | `<h1>, <h2>, <h3>, etc.` | `<td> or <span>` |
  | `<link type=”text/css”>` | `<td style=””>` |
  | `margin` | `<td style=”padding:;”>` |
  | `float` | `multiple table cells and align` |

 
  
## **Quick tips:**  
  
  
1. **Remember the full path** of the image and use your own server to upload the images with its convenient name.  
  
2. **Checking the ISP** before sending out thousands of emails, people with think you are a spammer.  
  
3. **Always test your design.** many emails clients has different perspectives on viewing the emails design.  
  
4. **Dont go over 600px** width. the ideal email width is 600px.  
  
5. **Use your footer like a footer**. This is a great place for lots of things including phone numbers and addresses, about information, unsubscribe options, and perhaps a little reminder of what this email is and why the reader is on the list.  
  
6. **Never use Javascript.** Because it will not work with most of the  email clients, and can have your Newsletter marked as spam.  
  
7. **Don't use <body> Tag.** It has been ignored in most of the email services
