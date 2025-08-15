<template>
    <div class="header">
        <div class="name">
            <i class="fas fa-a" ></i> 
            <span class="icon-text">Asude Ruken Kalğı</span>
        </div>
        <div class="sections">
            <a href="#about">About</a> 
            <a href="#projects">My Projects</a>  
            <a href="#accounts">Social Media Accounts</a> 
            <div class="mode-icons">
                <i class="fa-regular fa-sun" @click="$emit('toggleTheme')" v-if="!isDark"></i>
                <i class="fa-solid fa-moon" @click="$emit('toggleTheme')" v-if="isDark"></i>
            </div>
        </div>
    </div>
    <div class="line"></div>
</template>

<script>
export default{
    props:['isDark']
}
</script>


<style>
html{
    background-color: rgb(219, 217, 217);
    scroll-behavior: smooth;
}
.header{
    background-color: rgb(255, 255, 255);
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
    flex-wrap: wrap;
}
.sections{
    display: flex;
    letter-spacing: 1px;
    gap:1rem
}
.sections a{
    margin:10px;
    text-decoration: none;
    color:rgb(0, 0, 0);
    font-size: 20px;
    padding:10px 15px;
    border: 0.1px solid transparent; 
    border-radius: 15px;
    transition: all 0.3s ease;
    font-size: 18px;
}
.name{
    margin:10px;
    text-decoration: none;
    color:rgb(0, 0, 0);
    font-size: 25px;
    padding:10px 15px;
}
.sections a:hover{
    border:0.1px solid rgb(154, 154, 154);
    border-radius: 15px;
    padding:10px 15px;
    transition: all 0.3s ease;
    box-shadow: inset 0 0 5px rgba(0,0,0,0.2); 

}
.fas{
    background-color: rgb(0, 0, 0);
    border-radius: 40%;
    font-size: 20px;
    padding:5px 10px;
    color:white
}
.name{
    display: inline-flex;
    overflow: hidden;
}
.icon-text{
    opacity: 0;
    transform: translateX(-50px);
    animation: slideIn 1s forwards 0.6s; /* sayfa yüklenince gelsin */
    margin-left: 10px;
    font-weight: bold;
    letter-spacing: 2px;
}

@keyframes slideIn {
    to {
        opacity: 1;
        transform: translateX(0);
    }
}
.line{
    border-bottom: 2px solid black;
}
.mode-icons{
    font-size: large;
    padding: 1.2rem;
    width: 50px;
    cursor: pointer;
}
</style>