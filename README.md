# contact-footer-forms

# Contact Footer Forms

Converting website visitors to customers or quality leads starts with providing convenient ways for users submit contact information. [Solodev's](https://www.solodev.com/) stylized contact form for the footer of your website provides visitors with the convenience of submiting information no matter the page they visit. The form additionally includes full validation and stylized dropdowns via Selectize.


## Tutorial

For detailed instructions, view Solodev's [Convert More Website Visitors with Contact Footer Forms](https://www.solodev.com/blog/web-design/code-examples/convert-more-website-visitors-with-contact-footer-forms.stml) article.

## Demo

Check out a working example on [JSFiddle](https://jsfiddle.net/solodev/fcnmw00w/).

## HTML

The form includes basic HTML markup:
```
<form id="contentForm" name="contentForm" enctype="multipart/form-data" method="post" action="" data-h5-instanceid="0" novalidate="novalidate">
	<div class="col-md-12">
		<h2 class="text-uppercase ct-header ct-header--smaller ct-header--underline">
		   we are ready for your next project
		</h2>
		<div class="form-divider"></div>
		<p id="eval-anchor">
		   Thanks again for looking over our website and considering us for help with your project. Please take a moment and fill out as much of the form below as you can, and someone will quickly respond to your inquiry.
		</p>
		
		<div class="row">
			   <div class="col-md-8">
			   <div class="form-group">
				  <label class="sr-only" for="name">Name</label>
				  <input name="formfields[name]" id="name" class="form-control validate[required]" type="text" value="" placeholder="Name *">
			   </div>
			   </div>
			   <div class="col-md-4">
			   <div class="form-group">
				  <label class="sr-only" for="email">Email</label>
				  <input name="formfields[email]" id="email" class="form-control validate[required,custom[email]]" type="email" value="" placeholder="Email *">
				  <input type="hidden" name="formfields[fromEmail]" id="fromEmail" value="">
			   </div>
			</div>
		</div>
		
		<div class="row">
			<div class="col-md-4">
			   <div class="form-group">
				  <label class="sr-only" for="phone">Phone</label>
				  <input name="formfields[phone]" id="phone" class="form-control h5-phone validate[required,custom[phone]]" type="tel" value="" placeholder="Phone *"> 
			   </div>
			</div>
			<div class="col-md-4">
			   <div class="form-group">
				  <label class="sr-only" for="company">Company / Organization</label>
				  <input name="formfields[company]" id="company" class="form-control validate[required]" type="text" value="" placeholder="Company / Organization *">
			   </div>
			</div>
		   <div class="col-md-4">
			  <div class="form-group">
				<label class="sr-only" for="projecttype">Topic</label>
				<select class="form-control selectized" id="projecttype" name="Project Type" placeholder="Topic" tabindex="-1"> 
				  <option value="">Your Topic</option>
				  <option value="Topic Type 1">Project Type 1</option>
				  <option value="Topic Type 2">Project Type 2</option>
				  <option value="Topic Type 3">Project Type 3</option>
				</select>
			  </div>
		   </div>
		</div>
		
		<div class="form-group form-group--wide">
			<label class="sr-only" for="details">How Can We Help You?</label>
			<textarea name="formfields[details]" rows="5" id="details" class="form-control validate[required]" placeholder="How Can We Help You? *" cols="30"></textarea>
		</div>

		<button class="btn btn-primary btn-form" type="submit">Send</button>
		  
	</div>
</form>
```

## CSS

All CSS is included in footer-contact-form.css.

## JavaScript

The form uses several external dependencies, including [jQuery Validation Engine](https://github.com/posabsolute/jQuery-Validation-Engine) and [Selectize](https://github.com/selectize/selectize.js). The jQuery validation is used to ensure a website visitor fills in all required fields. The Selectize plugin is used to stylize the form's dropdown menu. These two plugins must be initialized with the following code:
```
<script>
	$(document).ready(function(){
		$("#contentForm").validationEngine('attach', {});
		$('#projecttype').selectize();
	});
</script>
```

For more information about customizing these plugins, visit [jQuery Validation Engine](https://github.com/posabsolute/jQuery-Validation-Engine) and [Selectize](https://github.com/selectize/selectize.js) on GitHub. The necessary assets for these plugins are contained in this repository under the "assets" folder.

## External Includes

The form includes the following third-party resources:
```
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" rel="stylesheet" type="text/css"/>
	
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js" type="text/javascript"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" type="text/javascript"></script>
```