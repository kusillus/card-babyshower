<template>
	<div class="hello">
		<div class="card-container">
			<div class="card">
				<div class="container-portada">
					<div class="portada">
					</div>
				</div>
				<div class="player"></div>
				<div class="container-text">
					<div class="text-one">
						TE INVITO A MI
					</div>
					<div class="text-two">
						BABYSHOWER
					</div>
				</div>
				

				<!-- <img src="../assets/bg_bomberman.png" alt=""> -->
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  
  bg_banner: require('../assets/bg_bomberman.png'),
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@font-face {
    font-family: 'endless';
    src: url('../fonts/EndlessBossBattle.ttf');
}
.hello{
	background-image: linear-gradient(45deg,#9f70b7, #7fddf7);
	width: 100%;
	min-height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
}
.card-container{
	min-width: 30rem;
	background: black;
	padding:40px;
	box-sizing: border-box;
	height: 500px;
}
.card{
	/* background: white; */
	position:relative;
}
.container-portada{
	overflow: hidden;
    position: relative;
    height: 300px;
}
.portada{
	// background: url('../assets/bg_bomberman.png');
	background: url('https://cdn.dribbble.com/users/264259/screenshots/4598107/p1omegaattackbg.gif');
    width: 100%;
    height: 320px;
    background-position: center;
    background-size: cover;
    position: absolute;
    background-position-y: 37px;
	transform: skewY(-12deg);
    top: -64px;
}
.container-text{
	font-family: endless;
	position: absolute;
    width: 100%;
    transform: rotate(-12deg);
    // background: orange;
    top: 261px;
	transform: skewY(-12deg);
}
.text-{
	&one{
		font-size: 30px;
		color: #f5f5f5;
		
	}
	&two{
		// color: #fb8dcc;
		color: #31dcff;
		font-size: 60px;
	}
}
.player{
	background: url('../assets/bomberman.png');
	top: 80px;
    left: 8px;
    position: absolute;
    width: 270px;
    height: 270px;
    background-size: cover;
    transform: scaleX(-1);
    z-index: 9999;
}
</style>
