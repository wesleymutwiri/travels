<script>
	import {
		afterUpdate
	} from 'svelte';

	afterUpdate(() => {
		const selectElement = (s) => document.querySelector(s);
		//open menu on click 
		function open() {
			selectElement('.nav-list').classList.add('active');
		}
		// close menu
		selectElement('.close').addEventListener('click', () => {
			selectElement('.nav-list').classList.remove('active');
		});
	})
</script>

<header>
	<div class="container">
		<nav>
			<div class="nav-brand">
				<a href="#">
					<img src="/images/logo.png" alt="">
				</a>
			</div>
			<div class="menu-icons open" on:click|once={open}>
				<i class="icon ion-md-menu"></i>
			</div>
			<ul class="nav-list">
				<div class="menu-icons close">
					<i class="icon ion-md-close"></i>
				</div>
				<li class="nav-item">
					<a href="" class="nav-link current">Home</a>
				</li>
				<li class="nav-item">
					<a href="" class="nav-link">Destination</a>
				</li>
				<li class="nav-item">
					<a href="" class="nav-link">Pricing</a>
				</li>
				<li class="nav-item">
					<a href="" class="nav-link">Booking</a>
				<li class="nav-item">
					<a href="" class="nav-link">About</a>
				</li>

			</ul>
		</nav>
	</div>
</header>
<main>


	<section class="hero">
		<div class="container">
			<div class="main-message">
				<h3>The Great outdoor</h3>
				<h1>Adventure</h1>
				<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur, saepe in? Corporis praesentium
					repellendus necessitatibus eaque saepe cumque quo! Esse, nobis modi distinctio natus exercitationem
					perferendis veniam officiis tempora mollitia.</p>

			</div>
			<div class="cta">
				<a href="#" class="btn">Book Now</a>
			</div>
		</div>
	</section>
	<section class="experience-outdoors">
		<div class="container">
			<div class="title-heading">
				<h3>Experience</h3>
				<h1>The thrilling outdoors</h1>
				<p>Lorem ipsum dolor sit amet consectetur adipisicing</p>
			</div>
			<div class="activities-grid">
				<!-- grid item number 1 -->
				<div class="activities-grid-item star-gazing">
					<i class="icon ion-md-star"></i>
					<h1>Star Gazing</h1>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum minima possimus cum, non minus
						sit. Sint dolore illo quisquam perspiciatis quam harum, blanditiis deserunt nisi unde debitis
						repellendus quas repudiandae?</p>
				</div>
				<div class="activities-grid-item hiking">
					<i class="icon ion-md-compass"></i>
					<h1>Hiking</h1>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum minima possimus cum, non minus
						sit. Sint dolore illo quisquam perspiciatis quam harum, blanditiis deserunt nisi unde debitis
						repellendus quas repudiandae?</p>
				</div>

				<div class="activities-grid-item camping">
					<i class="icon ion-md-bonfire"></i>
					<h1>Camping</h1>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum minima possimus cum, non minus
						sit. Sint dolore illo quisquam perspiciatis quam harum, blanditiis deserunt nisi unde debitis
						repellendus quas repudiandae?</p>
				</div>
			</div>
		</div>
	</section>
	<section class="testimonials">
		<div class="container">
			<div class="testimonial">
				<div class="testimonial-text-box">
					<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatibus dolorum hic porro itaque
						enim eius exercitationem. Magni, dolorum reprehenderit. Aut numquam veritatis dolorem nisi
						sapiente totam quia voluptate beatae! Dignissimos.</p>
					<i class="icon ion-md-quote"></i>
				</div>
				<div class="testimonial-customer">
					<img src="images/profile-pic.jpg" alt="">
					<h1>Martin G.</h1>
				</div>
			</div>
		</div>
	</section>
	<section class="begin-adventure">
		<div class="container">
			<div class="title-heading">
				<h3>Let the</h3>
				<h1> Adventure Begin</h1>
				<p>Lorem ipsum dolor sit amet consectetur adipisicing</p>
			</div>
			<div class="adventure-grid">
				<!-- adventure grid item #1 -->
				<div class="adventure-grid-item">
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, sit. Voluptate placeat
						molestiae fugiat qui mollitia incidunt distinctio, fuga nostrum ipsa debitis est commodi
						laudantium quibusdam inventore iusto, cupiditate praesentium.
					</p>
				</div>
				<!-- adventure grid item #2 -->
				<div class="adventure-grid-item">
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, sit. Voluptate placeat
						molestiae fugiat qui mollitia incidunt distinctio, fuga nostrum ipsa debitis est commodi
						laudantium quibusdam inventore iusto, cupiditate praesentium.
					</p>
				</div>

			</div>
			<a href="#" class="btn">Book your adventure</a>
		</div>
	</section>
</main>

<footer>
	<p>&copy; 2020 Outdoors. All rights reserved.</p>
</footer>
<style>
	.container {
		width: 100%;
		max-width: 98rem;
		margin: 0 auto;
		padding: 0 1.5rem;
	}

	nav {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 1rem 0;
		border-bottom: 1px solid rgba(255, 255, 255, .2);
	}

	.nav-brand {
		width: 2rem;
	}

	.menu-icons i {
		font-size: 3.5rem;
		color: #fafafa;
		cursor: pointer;
	}

	.close i {
		color: #eb648c;
	}

	.nav-list {
		width: 25rem;
		height: 100vh;
		background-color: #d7d4ed;
		position: fixed;
		top: 0;
		right: -26rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		z-index: 1500;
		transition: all 650ms ease-in-out;
	}

	.nav-list .active {
		right: 0;
	}

	.close {
		position: absolute;
		top: 1rem;
		left: 1.5rem;
	}

	.nav-item {
		margin: 1.5rem 0;
	}

	.nav-link {
		font-size: 1.6rem;
		text-transform: uppercase;
		color: rgba(0, 0, 0, .7);
	}

	.hero {
		width: 100%;
		height: 80vh;
		background: linear-gradient(135deg, rgba(49, 24, 131, 0.9) 0%, rgba(72, 56, 149, 0.8) 100%), url("/images/header-bg.jpg") center no-repeat;
		background-size: cover;
		position: relative;
	}

	.hero::before {
		content: "";
		position: absolute;
		left: 0;
		bottom: -3px;
		width: 100%;
		height: 4.7rem;
		background: url("/images/wave-small.png") center no-repeat;
		background-size: cover;
	}

	.main-message {
		width: 100%;
		max-width: 50rem;
		color: #fafafa;
		text-transform: uppercase;
		transform: translate(20%);
	}

	.main-message h3 {
		font-size: 1.6rem;

	}

	.main-message h1 {
		font-family: 'Aldrich'sans-serif;
		font-size: 4rem;
		margin: 1rem 0;
	}

	.main-message p {
		text-transform: lowercase;
	}

	.btn {
		background-color: #eb648c;
		border-radius: 2rem;
		color: #fafafa;
		display: inline-block;
		margin-top: 10rem;
		padding: 1rem 2.5rem;
		text-transform: uppercase;
		transition: background-color 650ms;
	}

	.btn:hover {
		background-color: #ce587b;
	}

	/* experience the outdoors */
	.experience-outdoors {
		padding: 0;

	}

	.title-heading {
		text-align: center;
		text-transform: uppercase;
		margin-bottom: 10rem;
		color: rgba(0, 0, 0, .7);
	}

	.title-heading h3 {
		font-size: 1.4rem;
	}

	.title-heading h1 {
		font-family: 'Aldrich'sans-serif;
		font-size: 2rem;
		margin: .5rem 0 1rem;
	}

	.title-heading p {
		text-transform: lowercase;
	}

	.activities-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
		grid-gap: 2.5rem;
	}

	.activities-grid-item {
		height: 40rem;
		padding: 5rem;
		color: #fafafa;
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: center;
		cursor: pointer;
		z-index: 1;
	}

	.activities-grid-item::before {
		content: "";
		position: absolute;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 4.7rem;
		background: url("/images/wave-small.png") center no-repeat;
		z-index: -1;
	}

	.star-gazing {
		background: url("/images/stars.jpg") center no-repeat;
	}

	.hiking {
		background: url("/images/hiking.jpg") center no-repeat;
	}

	.camping {
		background: url("/images/camping.jpg") center no-repeat;
	}

	.activities-grid-item i {
		font-size: 4rem;
		color: #eb648c;
	}

	.activities-grid-item h1 {
		font-family: 'Aldrich'sans-serif;
		text-transform: uppercase;
		font-size: 1.7rem;
		margin: 2rem, 0;
	}

	/* testimonials */
	.testimonials {
		width: 100%;
		height: 80vh;
		background: linear-gradient(135deg, rgba(49, 24, 131, 0.9), rgba(72, 56, 149, 0.8) 100%), url("/images/testimonials-bg.jpg")center no-repeat fixed;
		background-size: cover;
		position: relative;
	}

	.testimonials::before {
		content: "";
		position: absolute;
		top: -3px;
		left: 0;
		width: 100%;
		height: 4.7rem;
		background: url("/images/wave-small-reversed.png") center no-repeat;
		background-size: cover;
	}

	.testimonial {
		width: 100%;
		color: #fafafa;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		text-align: center;
	}

	.testimonial .text-box {
		padding: 0 1.5rem;
		position: relative;
		margin-bottom: 2rem;
	}

	.testimonial .text-box i {
		position: absolute;
		top: -8rem;
		left: 50%;
		transform: translate(-50%);
		font-size: 8rem;
		color: #eb648c;
		opacity: .5;
		z-index: -1;
	}

	.testimonial-customer img {
		width: 10rem;
		height: 10rem;
		border-radius: 100%;
		border: 3px solid #eb648c;
	}

	/* begin-adventures section  */
	.adventure-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
		grid-gap: 2.5rem;
		margin-bottom: 2rem;
	}

	.adventure-grid-item p {
		color: rgba(0, 0, 0, .7);
	}

	footer {
		padding: 2.5rem 0;
		text-align: center;
		color: rgba(0, 0, 0, .7);
		background-color: #d7d4ed;
	}

	/* Media queries  */
	@media screen and (min-width: 350px) {
		.main-message {
			transform: translateY(40%);
		}
	}

	@media screen and (min-width: 470px) {
		.hero::before {
			height: 9.4rem;
			background: url("/images/wave-medium.png");
			background-size: cover;
		}

		.testimonials::before {
			height: 9.4rem;
			background: url("/images/wave-medium-reversed.png");
			background-size: cover;
		}
	}

	@media screen and (min-width: 700px) {
		header {
			height: 8rem;
		}

		.nav-brand {
			width: 3.5rem;
		}

		.nav-list {
			width: initial;
			height: initial;
			background-color: transparent;
			position: initial;
			top: initial;
			right: initial;
			flex-direction: row;
			transition: initial;
		}

		.menu-icons {
			display: none;
		}

		.nav-item {
			margin: 0 2.5rem;
		}

		.nav-link,
		.current {
			color: #fafafa;
			position: relative;
			font-size: 1.3rem;
		}

		.nav-link::before,
		.current::before {
			position: absolute;
			left: 0;
			bottom: -.5rem;
			background-color: #eb648c;
			height: 2px;
			width: 100%;
			transform: scaleX(0);
			transform-origin: left;
			transition: transform 650ms;
		}

		.current::before {
			transform: scaleX(1);
		}

		.nav-link:hover::before {
			transform: scaleX(1);
		}

		.hero {
			height: 80vh;
		}

		.main-message {
			transform: translateY(50%);
		}

		.title-heading h1 {
			font-size: 2.5rem;
		}

	}

	@media screen and (min-width: 950px) {
		.hero::before {
			height: 22.7rem;
			background: url("/images/wave-large.png");
			background-size: cover;
		}

		.testimonials::before {
			height: 22.7rem;
			background: url("/images/wave-large-reversed.png");
			background-size: cover;
		}
	}

	@media screen and (min-width: 1200px) {
		.hero {
			height: 75vh;
		}
	}
</style>