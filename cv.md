# This is my CV.

1. **First Name**: Stanislav, **Last Name**: Dobrovolskiy

2. **Contact Info**:
	* [email] - stad-777@yandex.ru
	* [telephone] - 8-928-810-05-00

3. **Summary**:
	* [my goal] - I want to be a frontend developer
	* [my wishes] - I want to work in a large IT-company, and transfer my knowledge and skills to other young and motivated people.

4. **Skills**:
	* [HTML]
	* [CSS]
	* [SASS]
	* [GULP]
	* [JavaScript]
	* [jQuery]

5. **Code examples**:

> HTML

```
<div class="header-contacts">
	<div class="container">
		<div class="row justify-content-between align-items-center">
		<div class="col-10 col-md-6 col-xl-4 text-left">
			<i class="fa fa-location-arrow"></i> г. Ставрополь
		</div>
		<div class="col-10 col-md-6 col-xl-4 text-center">
			<i class="fa fa-mobile"></i> +7 ( 928 ) 810-05-00 
		</div>
		<div class="d-none d-xl-block col-xl-4 text-right">
			<i class="fa fa-clock-o"></i> Время работы: ежедневно с 10:00 - 20:00
		</div>
		</div>
	</div>
</div> 	      
```

> SASS/CSS

```
.carousel-services
	background-color: $dark
	position: relative	
	width: 100%			
	.owl-item
		&:nth-child(2n+2)
			.carousel-services-item
				flex-direction: column
	&-item
		width: 100%
		color: #fff
		font-size: 1.125rem
		font-weight: 300
		position: relative
		display: flex
		flex-direction: column-reverse		
		&:hover
			.carousel-services-image
				opacity: 1	    
	.owl-nav
		position: absolute
		top: 0
		width: 100%
		> button.owl-prev,
		> button.owl-next
			width: 61px
			height: 61px
			line-height: 61px
			display: block
			background-color: rgba(#fff, 0.85)
			color: $dark			
			position: absolute
			text-align: center
			font-size: 28px
			outline: none
		.owl-prev
			left: 0			
		.owl-next
			right: 0
```

> JQUERY

```
$("form.callback").submit(function() { //Change
	var th = $(this);
	$.ajax({
		type: "POST",
		url: "mail.php", //Change
		data: th.serialize()
	}).done(function() {
		th.find('.success').addClass('active').css('display','flex').fadeIn();
		setTimeout(function() {
			// Done Functions
			th.find('.success').removeClass('active').fadeOut();
			th.trigger("reset");
		}, 3000);
	});
	return false;
});
```

> JavaScript

```
class Clock {
	constructor({ template }) {
		this.template = template
	}

	render() {
		let date = new Date();

		let hours = date.getHours();
		if(hours < 10) hours = '0' + hours;

		let mins = date.getMinutes();
		if(mins < 10) mins = '0' + mins;

		let secs = date.getSeconds();
		if(secs < 10) secs = '0' + secs;

		let output = this.template
			.replace('h', hours)
			.replace('m', mins)
			.replace('s', secs);

		console.log(output);	
	}

	stop() {
		clearInterval(this.timer);
	}

	start() {
		this.render();
		this.timer = setInterval(() => this.render(), 1000);
	}
}

let clock = new Clock({template: 'h:m:s'});
clock.start();
	
setTimeout(() => clock.stop(), 5000);
```

6. **Experience**:
	* [coding tests] - from site [learn.javascript](https://learn.javascript.ru/)
	* [my individual projects] - self-study (2 years & 6 month)

7. **Education**:
	books, video lectures, online learning  

8. **English**:
	I went to school with an advanced study of English, then University education,
	sometimes watch English channels on TV.