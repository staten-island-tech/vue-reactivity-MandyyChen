
<template>
  <div class="about">
    <h1>About the Game</h1>
    <hr class="separator">
    <h3>This is a ultra duper cute game where you can stare at cats. 
      <br> Please adjust the size of this website until it looks cute.
      The format is weird..!
    </h3>
    <h3> Stolen images and cats from Neko Atsume © </h3>
    <p> Hi Mr.Whalen, this is my secret message to you because when I was searching
    for Google fonts during class, I found this really special one. Since I became super
    invested in integrating this one font, I forgot to actually find a legitimate font for
    the rest of the website. Anyways I doubt you saw this and if you did, you probably
    didn't bother to read so tehe hehe thx for being a gr8 teacher!
    </p>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Redacted+Script:wght@300;400;700&display=swap');

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0px;
    margin: 0 20px;
  }
}

.about {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center; /* Center-align all text */
  padding: 0px;
  margin: 0 20px;
}

.separator {
  width: 100%; 
  border: none; 
  border-top: 1px solid #ded67c; 
  margin: 20px 0; 
}

p{
  font-family: "Redacted Script", cursive;
  font-weight: 400;
  font-style: normal;
  font-size: 35px;
}

</style>
