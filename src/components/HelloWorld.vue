<template>
  <div class="hello">
  <body>
  <header>
		<h1>Jeka Pesa</h1>
		<nav>
			<ul>
				<li><a href="#about">About</a></li>
				<li><a href="#projects">Projects</a></li>
				<li><a href="#cv">CV</a></li>
				<li><a href="#contact">Contact</a></li>
			</ul>
		</nav>
	</header>
  <main>
		<section id="about">
			<h2>About Me</h2>
			<p>Hi! I'm Jeka, a multimedia design student at EASV in Denmark, passionate about creating engaging and impactful visual experiences. Whether it's graphic design, web design, or multimedia production, I strive to create work that inspires and resonates with audiences.</p>
		</section>

		<section id="projects">
			<h2>Projects:</h2>
			<div class="project_images">
			<div class="project">
				<div class="overlay">
				<h3>Raccoon illustration</h3>
				</div>
				<img src="../assets/rakun.png" alt="Raccoon illustration" class="rac">
			</div>
			<div class="project">
				<h3>Viking illustration</h3>
				<img src="../assets/viking_logo.png" alt="Viking illustration" class="vik">
			</div>
			<div class="project">
				<h3>Mini me</h3>
				<img src="../assets/mini_me.png" alt="Mini me">
			</div>
			<div class="project">
				<h3>Child labour poster</h3>
				<img src="../assets/poster.png" alt="Poster">
			</div>
			<div class="project">
				<h3>Distillery shop logo</h3>
				<img src="../assets/logo_destillery_short.png" alt="Distillery shop">
			</div>
		</div>
		</section>

		<section id="cv">
			<h2>CV:</h2>
			<div class="cv-link">
				<a href="/pdf/CV JEKA PESA.pdf" target="_blank"><img src="../assets/pdf.png" alt="PDF CV"></a>
				<p>Download my PDF CV</p>
			</div>
			<div class="cv-link">
				<a href="https://youtu.be/KvoyodZPUPs" target="_blank"><img src="../assets/youtube.png" alt="Video CV"></a>
				<p>Watch my Video CV on YouTube</p>
			</div>
		</section>

        <section id="business-card">
		<h2>Business Card:</h2>
		<img src="../assets/business_card_front.png" alt="Business Card" class="business_card_front">
		<img src="../assets/business_card_back.png" alt="Business Card Back" class="business_card_back">
		</section>
</main>
<footer id="contact">
	<div class="footer-nav">
		<ul>
			<li><a href="#about">About</a></li>
			<li><a href="#projects">Projects</a></li>
			<li><a href="#cv">CV</a></li>
			<li><a href="#contact">Contact</a></li>
		</ul>
	</div>
	<div class="social-media">
		<a href="https://www.instagram.com/jeka_pesa/" target="_blank"><img src="../assets/instagram.png" alt="Instagram"></a>
		<a href="https://www.linkedin.com/in/jeka-pe%C5%A1a-596219269/" target="_blank"><img src="../assets/linkedin.png" alt="LinkedIn"></a>
	</div>
</footer>
</body>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
    color: white;
}

body {
	font-family: Arial, sans-serif;
   /* background-image: linear-gradient(#2a2f4f, #e5beec);*/
   background-size: contain;
   background-color: #7251B5;
    
}

body::-webkit-scrollbar {
    display: none;
  }

header {
	background-color: #7251B5;
	color: #fff;
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 10px 20px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 80px;
  z-index: 9999;
  box-shadow: 0 1px 10px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 50px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  animation: navbar-extend 1.8s ease-in-out forwards;
}

header h1{
    animation: fade-in 5s ease-in-out;
}

@keyframes fade-in {
    0%{
        opacity: 0%;
    }
    100%{
        opacity: 100%;
    }
}

@keyframes navbar-extend {
    0% {
      width: 0;
    }
    100% {
      width: 100%;
    }
  }

nav ul {
	list-style: none;
	display: flex;
}

nav ul li {
	margin-left: 20px;
}

nav ul li a {
	color: #fff;
	text-decoration: none;
}

main {
	padding: 50px 20px;
}

h2 {
	margin-bottom: 20px;
}

#about {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 30px;
    border-radius: 25px;
    margin-bottom: 50px;
    margin-top: 50px;
    background-color: rgba(255, 255, 255, 0.193);
    border-radius: 30px;
  }
  
  #about h2 {
    font-size: 32px;
    margin-bottom: 20px;
  }
  
  #about p {
    font-size: 16px;
    line-height: 1.5;
    text-align: center;
  }

.project {
	margin-bottom: 50px;
    flex-basis: calc(33.33% - 20px);
    min-width: 300px;
    max-width: 400px;
    overflow: hidden;
}

#projects {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-start;
    gap: 20px;
    background-color: rgba(255, 255, 255, 0.193);
    padding-top: 80px;
    border-radius: 30px;
  }

  .project_images{
    background-color: #C19EE0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-start;
  }

#projects h2{
    text-decoration: underline;
}

.project img {
	width: 250px;
	margin-bottom: 20px;
  margin-top: 5px;
  max-height: 250px;
  border-radius: 10px;
  transition: all 0.3s ease-in-out;
}
  
  .project img:hover {
    transform: scale(1.05);
    filter: brightness(70%);
    transition-delay: 0.2s;
  }

#cv {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 50px 0;
    text-align: center;
  }

  #cv h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    text-decoration: underline;
  }

.cv-link {
    display: flex;
    align-items: center;
    margin: 20px 0;
    background-color: rgba(255, 255, 255, 0.193);
    border-radius: 30px;
    padding: 15px;
}

.cv-link img {
	width: 50px;
  height: 50px;
  margin-right: 10px;
}

.cv-link p {
    font-size: 1.2rem;
    margin: 0;
  }

  #business-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
    background-color: #FDE2F3;
  }
  
  #business-card h2 {
    font-size: 2rem;
    text-align: center;
    margin-bottom: 10px;
    text-decoration: underline;
  }
  
    #business-card img {
    width: 400px;
    height: 200px;
    border-radius: 10px;
    box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.3);
    margin-bottom: 50px;
    margin-top: 50px;
    transition: all 0.3s ease-in-out;
    }

    #business-card img:hover {
        transform: scale(1.05);
        filter: brightness(70%);
        transition-delay: 0.2s;
      }

.contact-info p {
margin-bottom: 10px;
}

footer {
background-color: #000000;
color: #fff;
padding: 20px;
display: flex;
justify-content: space-between;
align-items: center;
}

.footer-nav ul {
list-style: none;
display: flex;
}

.footer-nav ul li {
margin-left: 20px;
}

.footer-nav ul li a {
color: #fff;
text-decoration: none;
}

.social-media img {
max-width: 50px;
height: auto;
margin-left: 20px;
cursor: pointer;
}

.rac{
  margin-right: 90px;
}
.vik{
  margin-right: 50px;
}

/* Media queries */

@media screen and (max-width: 768px) {
    header {
        flex-direction: column;
        text-align: center;
    }
    
    nav ul {
        margin-top: 20px;
    }
    
    nav ul li {
        margin: 0 10px;
    }
    
    #about {
        padding: 20px;
      }
      
      #about h2 {
        font-size: 28px;
      }
      
      #about p {
        font-size: 14px;
      }
    

    .project {
        display: flex;
        flex-basis: 100%;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    #projects {
        flex-direction: column;
        align-items: center;
      }
    
    .project img {
        max-width: 80%;
        margin-bottom: 10px;
    }

    #cv {
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
      }

    .cv-link {
        margin: 0;
    }
    
    .cv-link:first-child {
        margin-right: 50px;
    }
    
    .contact-info p {
        margin: 0;
    }
    
    .social-media img {
        margin: 0 10px;
    }
}

@media screen and (max-width: 480px) {
    footer {
        flex-direction: column;
        align-items: center;
    }
    
    .footer-nav ul {
        margin-bottom: 20px;
    }
    
    .social-media img {
        margin: 10px 0;
    }
}

/* Flexbox container */

.container {
display: flex;
flex-wrap: wrap;
justify-content: space-between;
}

/* Flexbox item */

.item {
flex-basis: calc(33.33% - 20px);
margin-bottom: 40px;
}

.item img {
max-width: 100%;
height: auto;
margin-bottom: 20px;
}

.item h3 {
margin-bottom: 10px;
font-size: 1.2rem;
font-weight: bold;
}

.item p {
margin-bottom: 20px;
font-size: 1rem;
line-height: 1.5;
text-align: justify;
}        
</style>
