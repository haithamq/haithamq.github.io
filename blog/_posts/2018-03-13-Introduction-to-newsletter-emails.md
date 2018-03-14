title: Introduction to newsletter emails  
comments: true  
\-\-\-  
  
Nowadays the email newsletter is taking a good advantages of marketing strategies. But it's not all about generating a random newsletters that will bring you a better conversion.  
There are some techniques and steps need to be followed in order to make a better newsletter.  
  
In my first blog post i will be talking from the technical side on how we can create or structure a Newsletter email and what are the things we need to consider while building those templates and how it will be  tested before we send it to the subscribers.  
  
 * __Email clients.__  

First of all we need to be aware that each email client like  (_Gmail 
, Yahoo, Outlook, Mail, etc_)  does not accept all the CSS properties and sometimes it will override it with it's own CSS. So we need to use sometimes an `!important` attribute. It means that
 > this is important, ignore subsequent rules, and any usual specificity issues, apply this rule!. 
 
For Example 

``` <span style="color:red !important;">hello world</span>``` 
  
Remember that some email clients will automatically transform typed out hyperlinks into links (if we don't anchor `<a>` them ourselves). This can sometimes achieve negative effects (say if we're putting a style on each of the hyperlinks to appear a different color).  
  

  
* __ In-line Css.__  
  
  
when we start developing a newsletter template we need to write an __Inline CSS__ for the most __HTML__ Tags. For an Example: 
  ``` <p style="color: red;">Hello World</p>  ``` because those Email clients won't reference external CSS files, because it might interfere with their own CSS coding. We recommend placing your CSS code in-line with your content instead of using body and head tags  
  
  
  
* __Tables or Divs?__  
  
  
  
Start using `<table>` instead of `<div>` tags to control our design layout and the structure of the newsletter email.  
  
When it comes to email __HTML__, note that all best practices from Web development goes out the window. We Should use Tablets instead of Divs. Because __HTML__ Tables are likewise supported by every major email client.  
  
So, if we want the email newsletter to display relatively well across email clients we need to use __HTML__ tables to lay out our newsletter campaigns.  
  
below it shows what __HTML__ tags we can use in building the newsletter email.  
  
  
 
  
  
  | Instead of this | Use this |
  | --- | --- |
  | ```<div>``` | ```<table>, <tr>, <td>``` |
  | ```<p>``` | ```<td>``` |
  | ```<h1>, <h2>, <h3>, etc.``` | ```<td> or <span>``` |
  | ```<link type=”text/css”>``` | ```<td style=””>``` |
  | ```margin``` | ```<td style=”padding:;”>``` |
  | ```float``` | ```multiple table cells and align``` |

 
  
# __Quick tips:__  
  
  
1. __Remember the full path__ of the image and use your own server to upload the images with its convenient name.  
  
2. __Checking the ISP__ before sending out thousands of emails, people with think you are a spammer.  
  
3. __Always test your design.__ many emails clients has different perspectives on viewing the emails design.  
  
4. __Dont go over 600px__ width. the ideal email width is 600px.  
  
5. __Use your footer like a footer__. This is a great place for lots of things including phone numbers and addresses, about information, unsubscribe options, and perhaps a little reminder of what this email is and why the reader is on the list.  
  
6. __Never use Javascript.__ Because it will not work with most of the  email clients, and can have your Newsletter marked as spam.  
  
7. __Don't use <body> Tag.__ It has been ignored in most of the email services
