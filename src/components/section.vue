<template>
    <div>
        <section id="about">
            <div class="about-text">
                <h1>HELLO <br> MY NAME IS ASUDE </h1>
                <p>I am a third-year computer engineering student at Karadeniz Technical University.</p>
            </div>
            <img src="c:\Users\asude\Desktop\WhatsApp Görsel 2025-06-06 saat 23.45.17_1136cec0.jpg" alt="">
        </section>
        <section id="projects">
            <h2 class="proj-title">MY PROJECTS</h2>
            <div class="proj-content">
                <div class="app">
                    <h2>Earthquake Rescue Application</h2>
                    <p>
                    A mobile application designed to quickly share the locations and information of people trapped under debris after an earthquake with authorities and the public. Authorities can track these locations on a map and update the status of rescued individuals.
                    </p>
                    <p class="tech">Technology: Flutter</p>
                    <button @click="openGithub">Github Project</button>
                </div>
                <div class="app">
                    <h2>Sigortam.net application interface</h2>
                    <p>
                        I created the interface of the Sigortam.net application using pure JavaScript.
                    </p>
                    <p class="tech">Technology: HTML CSS JavaScript</p>
                    <button @click="openGithub2">Github Project</button>
                </div>
                <div class="app">
                    <h2>Calculator Application</h2>
                    <p>  
                        This calculator app can calculate all operations. It is written in pure JavaScript.
                    </p>
                    <p class="tech">Technology: HTML CSS JavaScript</p>
                    <button @click="openGithub3">Github Project</button>
                </div>
            </div>
        </section>
        <section id="accounts">
            <h2 class="accounts-title">CONTACT & ACCOUNTS</h2>
            <div class="icons">
                <i class="fa-brands fa-github" @click="openGit"></i>
                <i class="fa-brands fa-linkedin" @click="openLinkedin"></i>
                <i class="fa-solid fa-envelope" @click="openMail"></i>
            </div>
        </section>
    </div>
</template>

<script>
export default{
    methods:{
        openGithub(){
            window.open('https://github.com/asude2/softwareEngineering_project.git')
        },
        openGithub2(){
            window.open('https://github.com/asude2/sigortamnetArayuz.git')
        },
        openGithub3(){
            window.open('https://github.com/asude2/hesapMakinesi.git')
        },
        openGit(){
            window.open('https://github.com/asude2')
        },
        openLinkedin(){
            window.open('https://www.linkedin.com/in/asude-kalg%C4%B1-826006286/')
        },
        openMail(){
            window.location.href="mailto:asuderuken63@gmail.com";
        }
    }
}
</script>

<style scoped>
/* about section */
#about{
    display: flex;
}
.about-text{
    margin:7rem 5rem;
    color:rgb(91, 91, 91);
}
#about h1{
    font-size: 40px;
}
#about p{
    font-size: 20px;
    color:rgb(0, 0, 0);
}
#about img{
    height: 300px;
    width: auto;
    margin: 5rem 8rem;
    border-radius: 100%;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.8);
}


/* project section */
#projects{
    background-color: rgb(65, 65, 65);
    padding:1rem
}
.app{
    width:250px;
    background-color:  rgb(219, 217, 217);
    margin: 1rem;
    padding:0.8rem 2rem;
    border-radius: 5rem;
    box-shadow: 0 4px 15px rgba(0,0,0,1);
    display: flex;
    flex-direction: column;
    justify-content: space-between; 
}
.app button{
    border:solid 1px rgb(118, 117, 117);
    background-color: rgb(193, 192, 192);
    padding:0.5rem;
    border-radius: 1rem;
    cursor: pointer;
    border-end-end-radius:inherit;
    margin-left:10rem;
    margin-bottom:0
}
.tech{
    font-weight: 600;
    font-size: 16px;
    color:rgb(69, 69, 69)
}
.app button:hover{
    background-color: rgb(214, 213, 213);
    border:solid 1px rgb(143, 142, 142);
}
.proj-title{
    color:rgb(190, 190, 190);
    margin-bottom: 3rem;
    margin-left: 5rem;
    letter-spacing: 2px;
    font-size: 40px;
}
.proj-content{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

/*accounts section*/ 
.accounts-title{
    color:rgb(65, 65, 65);
    letter-spacing: 2px;
    font-size: 40px;
    margin-top: 4rem;
    display: flex;
    justify-content: center;
}
.icons{
    font-size: 2rem;
    display: flex;
    margin-top: 3rem;
    margin-bottom: 3rem;
    justify-content: center;
}
.icons i{
    margin:0 2rem;
    transition: transform 0.3s ease;
}
.icons i:hover{
    transform: scale(1.2);
    cursor: pointer;
}

</style>

