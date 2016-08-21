---
layout: post
title: "Second Day at Workshop"
date: 2016-08-01 03:29:50 +0300
comments: true
categories: 
---

<p>		We started to second day with simple html lesson.As all we know Html is a markup language using for websites.It stands for HyperText Markup Language and it is a milestone for  web pages because everything in the internet uses this language.All other languages or tools you know like php, .net, rails are just a tool for transforming our code to HTML.because of that knowing html is most important thing for a web developper.After we finished talking about html we passed on another tool we use in rails environment to transform our code to html.It is a gem called Haml.  
</p>
<p> 	Haml is a templating engine that makes you write html easily.It eliminates unnecessary tag system
and uses indentation to  tidy up your code.By removing the unnecessary tags it makes your code cleaner 
and easy to understand.
</p>
{% codeblock %}
	%nav.navbar.navbar-default
        .container-fluid
          / Brand and toggle get grouped for better mobile display
          .navbar-header
            %button.navbar-toggle.collapsed{"aria-expanded" => "false", "data-target" => "#bs-example-navbar-collapse-1", "data-toggle" => "collapse", :type => "button"}
              %span.sr-only Toggle navigation
              %span.icon-bar
              %span.icon-bar
              %span.icon-bar
           = link_to 'Blog', root_path, class: 'navbar-brand'
{% endcodeblock %} 
<p>		Here is some  haml example code we wrote in class.We tried to write a navigation bar for our blog website.As you can see tagnames didnt change.We just used different characters to write the tags.
</p>
<p>	Css was the other subject we mentioned that day.As you know css is the other important part of web developing along with JavaScript.Css stands for cascading style sheets and often used to set the visual stle of webpages and styling the pages.
</p>
<p>	In class we found opportunity to practice our css skills.Ms. Kapi told us to  create a html button without using bootsrap.The example code what we did is given down below.
</p>
{% codeblock %}
		.btn {
		  border-radius: 28px;
		  font-family: Arial;
		  color: #ffffff;
		  font-size: 20px;
		  background: #d91a1a;
		  padding: 10px 20px 10px 20px;
		  text-decoration: none;
		}
{% endcodeblock %}
<p> After these small assignments we pass on the other subjects like bootstrap and sass.We mentioned about how we import to use css and bootstrap files.How we change the extensions of the files.That's what I'm gonna talk about now.Befor using Css or bootstrap we have to import the css file we're workin on the application.css file.Regarding the tool what we use, we have to change the extebsion of the files including the application.css file.If we're going to use pure bootstrap and css we change it to style.css.scss.If we're going to use sass we change it the extension to style.css.sass  
</p>
<h4>Sass</h4>
<p>	So the sass is another tool for styling web pages and interpret into css.It stands for Syntactically Awesome Stylesheets.The official implementation of Sass is open-source and coded in Ruby; however, other implementations exist, including PHP, and a high-performance implementation in C called libSass.	
</p>
<p> Best things about sass are the mechanisms that it provides us.First of all you can write cleaner css code in sass.It also gets rid of the unnecessary  characters and leaves easier and cleaner code. 
</p>
<p>This is how it looks a simple css code:</p>
{% codeblock %}
.content-navigation {
  border-color: #3bbfce;
  color: darken(#3bbfce, 10%);
}

.border {
  padding:  16px ;
  margin:  16px;
  border-color: #3bbfce;
}
{% endcodeblock %}
<p>This is the sass version the same code:</p>
{% codeblock %}
.content-navigation 
  border-color: #3bbfce;
  color: darken(#3bbfce, 10%);

.border
  padding:  16px ;
  margin:  16px;
  border-color: #3bbfce;
{% endcodeblock %}
<h5>Variables</h5>
<p>	Unlike the css, sass has the ability to store information within your stylesheet. You can store things like colors, font stacks, or any CSS value you think you'll want to reuse.Sass uses the $ symbol to make something a variable. Here's an example:
</p>
{% codeblock %}
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body 
  font: 100% $font-stack;
  color: $primary-color;

{% endcodeblock %}
<h4>Nesting</h4>
<p>	Like haml and html codes, sass lets you nest the objects within each other so you dont have to use 
unique ids and classes.It allows you to design every object differenly even the same kind of objects.  
</p>
<p>In sass style your code would look like this</p>
{% codeblock %}
table.hl 
  margin: 2em 0
  td.ln 
    text-align: right
  
li 
  font: 
    family: serif
    weight: bold
    size: 1.3em
{% endcodeblock %}
<p>But in css style:</p>
{% codeblock %}
table.hl {
  margin: 2em 0;
}
table.hl td.ln {
  text-align: right;
}

li {
  font-family: serif;
  font-weight: bold;
  font-size: 1.3em;
}
{% endcodeblock %}
<h4>Mixins</h4>
<p> In CSS any repeating code in your stylesheet must must written over and over again.Another awesom mechanism that Sass gave us is mixins.You can store your repeated codes in mixins and when you are using it you can use just the mixins names.Just like the functions, you can even pass some parameters in your mixins to mame your mixins more flexible.Here's an example for border-radius.</p>
{% codeblock %}
=border-radius($radius)
  -webkit-border-radius: $radius
  -moz-border-radius:    $radius
  -ms-border-radius:     $radius
  border-radius:         $radius

.box
  +border-radius(10px)
{% endcodeblock %}
<h4>Inheritance</h4>
<p>In Sass, inheritance is achieved by inserting a line inside of a code block that uses the @extend keyword and references another selector. The extended selector's attributes are applied to the calling selector.</p>
<p>Here is an example of how we can use extend keyword:</p>
{% codeblock %}
.error
  border: 1px #f00
  background: #fdd

.error.intrusion 
  font-size: 1.3em
  font-weight: bold

.badError 
  @extend .error
  border-width: 3px
{% endcodeblock %}
<p>This code would look like this in classic CSS style</p>
{% codeblock %}
.error, .badError {
  border: 1px #f00;
  background: #fdd;
}

.error.intrusion,
.badError.intrusion {
  font-size: 1.3em;
  font-weight: bold;
}

.badError {
  border-width: 3px;
}
{% endcodeblock %}

<h3>Compass</h3>
<p>Compass is an open-source CSS authoring framework that supports sass make writing stylesheets powerful and easy.Compass also allows you to get rid of unnecassary repetitions in your style sheet with sass it gives you more powerful ann cleaner code structure.</p>
<p>Here is some some sass code with compass:</p>
{% codeblock %}
@import compass/css3
 
@import compass/utilities
 
#demo
  +clearfix
 
.border-radius-example
  width: 125px
  height: 125px
  background: red
  margin: 20px
  float: left
  padding: 5px
 
#border-radius
  +border-radius(25px)
 
#border-radius-top-left
  +border-top-left-radius(25px)
 
#border-radius-top-right
  +border-top-right-radius(25px)
 
#border-radius-bottom-left
  +border-bottom-left-radius(25px)
 
#border-radius-bottom-right
  +border-bottom-right-radius(25px)
 
#border-radius-top
  +border-top-radius(25px)
 
#border-radius-bottom
  +border-bottom-radius(25px)
 
#border-radius-left
  +border-left-radius(25px)
 
#border-radius-right
  +border-right-radius(25px)
 
#border-radius-combo
  +border-corner-radius(top, left, 40px)
  +border-corner-radius(top, right, 5px)
  +border-corner-radius(bottom, left, 15px)
  +border-corner-radius(bottom, right, 30px)
{% endcodeblock %}
<p>this is the same code in css, look how long it looks </p>
{% codeblock %}
#demo {
  overflow: hidden;
  *zoom: 1;
}
 
.border-radius-example {
  width: 125px;
  height: 125px;
  background: red;
  margin: 20px;
  float: left;
  padding: 5px;
}
 
#border-radius {
  -moz-border-radius: 25px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
}
 
#border-radius-top-left {
  -moz-border-radius-topleft: 25px;
  -webkit-border-top-left-radius: 25px;
  border-top-left-radius: 25px;
}
 
#border-radius-top-right {
  -moz-border-radius-topright: 25px;
  -webkit-border-top-right-radius: 25px;
  border-top-right-radius: 25px;
}
 
#border-radius-bottom-left {
  -moz-border-radius-bottomleft: 25px;
  -webkit-border-bottom-left-radius: 25px;
  border-bottom-left-radius: 25px;
}
 
#border-radius-bottom-right {
  -moz-border-radius-bottomright: 25px;
  -webkit-border-bottom-right-radius: 25px;
  border-bottom-right-radius: 25px;
}
 
#border-radius-top {
  -moz-border-radius-topleft: 25px;
  -webkit-border-top-left-radius: 25px;
  border-top-left-radius: 25px;
  -moz-border-radius-topright: 25px;
  -webkit-border-top-right-radius: 25px;
  border-top-right-radius: 25px;
}
 
#border-radius-bottom {
  -moz-border-radius-bottomleft: 25px;
  -webkit-border-bottom-left-radius: 25px;
  border-bottom-left-radius: 25px;
  -moz-border-radius-bottomright: 25px;
  -webkit-border-bottom-right-radius: 25px;
  border-bottom-right-radius: 25px;
}
 
#border-radius-left {
  -moz-border-radius-topleft: 25px;
  -webkit-border-top-left-radius: 25px;
  border-top-left-radius: 25px;
  -moz-border-radius-bottomleft: 25px;
  -webkit-border-bottom-left-radius: 25px;
  border-bottom-left-radius: 25px;
}
 
#border-radius-right {
  -moz-border-radius-topright: 25px;
  -webkit-border-top-right-radius: 25px;
  border-top-right-radius: 25px;
  -moz-border-radius-bottomright: 25px;
  -webkit-border-bottom-right-radius: 25px;
  border-bottom-right-radius: 25px;
}
 
#border-radius-combo {
  -moz-border-radius-topleft: 40px;
  -webkit-border-top-left-radius: 40px;
  border-top-left-radius: 40px;
  -moz-border-radius-topright: 5px;
  -webkit-border-top-right-radius: 5px;
  border-top-right-radius: 5px;
  -moz-border-radius-bottomleft: 15px;
  -webkit-border-bottom-left-radius: 15px;
  border-bottom-left-radius: 15px;
  -moz-border-radius-bottomright: 30px;
  -webkit-border-bottom-right-radius: 30px;
  border-bottom-right-radius: 30px;
}
{% endcodeblock %}

<p>Other part of the day we contiuned  to learn cybele gem. Mr Akbudak, first explained us, how user managament part works.We looked over the every part of user managment system.After that we fix the error we saw from the other day.We changed the name  of user profile file in conrtrollee</p>
<p>To solve profile update error we changed some miswriting in the progile_controller in user file.
Here is the changes we did </p>
{% codeblock %}
1   def show
2     add_breadcrumb @profile.full_name, user_profile_path
3     respond_with([:user, @profile])    
4   end
{% endcodeblock %}
<p>We deleted the square brackets in third line and we did the same for the update action in the same file</p>
<p>Some part of the lesson we learned to send messages to users in this case to admins.We learned to send to send a welcome message  after adding a new admin.To do that we added a new function to admin_mailer class.İt takes admin's Id, finds the admin and sets to email adres and subject </p>
{% codeblock %}
  def welcome(admin_id)
    @admin      = Admin.find admin_id
    @subject =t('email.admin.welcome.title')
    mail(to: @admin.email, subject: @subject)
  end
{% endcodeblock %}
<p>After that we added an another fuction called send_welcome_message to send a message what we want and within this we call the welcome function what we write in the admin_mailer.rb file.To show a messaga we want we create  a file with the same name in the other function in the admin_mailer which is welcome.
 </p>
 {% codeblock %}
  def welcome_message_send
    AdminMailer.welcome(self.id).deliver_later!
  end
{% endcodeblock %}
<p>This is the function we write in models</p>
 {% codeblock %}
  %h2= t('Welcome To Page') 
{% endcodeblock %}
<p>This is the simple view file to show the message we send.And don forget to add your function after commit action because that what sends your message to created admin.</p>
 {% codeblock %}
   after_commit :send_login_info,:welcome_message_send, on: :create
{% endcodeblock %}
<P>We continued some coding like thise for a while after that we learned how to deploy our app to heroku
</P>
<p>We dowloaded and installed heroku toolbelt with code down below.It took a lot of our time to install.
At the end, I couldn't even use because I got an error.So ı couldn't login to heroku.I had to just listen to class instead of doing it..:(</p>
{% codeblock %}
	wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh
{% endcodeblock %} 
<p>As I learned after we install, we needed to clone our project to git if we're using git to deploy.Theb we got into our prject folder and use create command for heroku</p>
{% codeblock %}
	heroku create
{% endcodeblock %}
<p> When we create an app, a git remote (called heroku) is also created and associated with your local git repository.
	Heroku generates a random name for your app, or you can pass a parameter to specify your own app 
name.After that we deploy our project with this code	
</p>
{% codeblock %}
	git push heroku master
{% endcodeblock %}
<p>The project is now deployed.To open project we deploy, we just run the code:</p>
{% codeblock %}
	 heroku open
{% endcodeblock %}
<p>This wasn't all i learn from workshop but just all I can write here.Again I am really 
appreciated for all my theacher's efforts and time that they spare from their actual jobs.And thank you giving me some homeworks to keep me doing something important other than playing Dark Souls and FarCry.I haven't got the chancew to practice cybele yet but  I am eager to learn more about it.</p> 
