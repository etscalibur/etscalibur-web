
<style>
  *{ font-family: 'Poppins', sans-serif;}
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;    
    padding : 30px;
    background-color: var(--bg-color);
    color: var(--text-primary);
    text-align: center;
  }
  h1 {
    font-family: 'Cyberion';
    font-weight: normal;
    font-style: normal;

    font-size: 3rem;
    margin-bottom: 0.5rem;
    color: var(--primary-color); /* Bright color for the title */
  }

  p {
    font-size: 1.2rem;
    max-width: 600px;
    margin: 1rem 0;
    line-height: 1.5;
    
  }

  .cta {
    background-color: var(--button-p);
    color: var(--button-p-text);
    padding: 0.8rem 2rem;
    border: none;
    border-radius: 5px;
    font-size: 1.2rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .cta:hover {
    background-color: var(--button-p-hover); /* Lighter shade on hover */
  }

  .robot-image {
    margin-top: 2rem;
    width: 300px;
    height: auto;
  }

 
</style>
<div class="container">

  <h1>Bienvenue !</h1>
  <p>
  Êtes-vous prêt à libérer la puissance de votre créativité et de vos compétences en ingénierie ? Rejoignez-nous pour concevoir, construire et combattre nos propres robots de combat !
Que vous soyez novice ou professionnel chevronné, il y a une place pour vous ici. Commençons ensemble le chemin vers la victoire !
  </p>
  <button class="cta" on:click={() => alert('Get ready to rumble!')}>Rejoins la bataille!</button>
  <img src="https://i.pinimg.com/originals/07/e8/2e/07e82eb13044b7346f479c4c9d3a39cf.png" alt="Fighting Robot" class="robot-image" />
</div>
