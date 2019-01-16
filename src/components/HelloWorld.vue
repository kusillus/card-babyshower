<template>
	<div class="hello" @click="showModal = !showModal">
		<div class="card-container" >
			<div class="card">
				<div class="container-portada">
					<div class="portada">
					</div>
				</div>
				<div class="player"></div>
				<div class="bomb"></div>
				<div class="container-text">
					<div class="text-one">
						TE INVITO A MI
					</div>
					<div class="text-two">
						BABYSHOWER
					</div>
					<div class="text-three">
						CLICK PARA VER DETALLE
					</div>
				</div>
				

				<!-- <img src="../assets/bg_bomberman.png" alt=""> -->
			</div>
		</div>
		<div class="modal" v-show="showModal">
			<div class="card-modal">
				<div>
					<strong>Lugar:</strong>
					<span>La ubicaciones del babyshower</span>
				</div>
				<div>
					<strong>Lugar:</strong>
					<span>La ubicaciones del babyshower</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
	  return {
		  showModal: false
	  }
  },
  methods: {
	  showDetails: function() {
		  console.log('detalles')
	  }
  }
  
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
.modal{
	position: absolute;
    background: #00000078;
    z-index: 99000;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.card-modal{
	width: 280px;
    background: #fff;
    padding: 15px;
    box-sizing: border-box;
    border-radius: 4px;
}
.card-container{
	cursor: pointer;
	max-width: 30rem;
	background: black;
	padding:55px;
	box-sizing: border-box;
	height: 500px;
	width: 100%;
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
		color: #31dcff;
		font-size: 60px;
		transition: all 2s;
		animation: textcolor 3s infinite;
	}
	&three{
		color: white;
	}
}

@media (max-width: 450px) {
  .card-container {
    max-width: 30rem;
	height: 440px;
	padding:35px;
	.portada{
		height: 305px;
	}
	.player{
		top: 85px;
		left: -20px;
		position: absolute;
		width: 200px;
		height: 200px; 
	
	}
	.container-text{
		top: 269px;
		.text-{
			&one{
				font-size:20px;
			}
			&two{
				font-size:40px;
			}
			&three{
				font-size: 15px;
			}
		}
	}
  }
}

@keyframes textcolor {
	0%{
		color: #ff6200;
	}
	30% {
		color: #e5ec05;
	}
	60%{
		color: #f642ff;
	}
	90% {
		color: #31dcff;
	}
}
.player{
	background: url('../assets/bomberman.png');
	top: 20px;
    left: -22px;
    position: absolute;
    width: 270px;
    height: 270px;
    background-size: cover;
    transform: scaleX(-1);
    z-index: 9999;
}
.bomb{
	background: url('../assets/bomb.png');
	top: 20px;
    right: 8px;
    position: absolute;
    width: 140px;
    height: 140px;
    background-size: cover;
	z-index: 9995;
	animation: bomb 1s infinite; 
}
@keyframes bomb {
	0% {
		width: 140px;
    	height: 140px;
		top: 20px;
    	right: 8px;
	}
	// 30% {
	// 	width: 160px;
    // 	height: 160px;
		
	// }
	50% {
		width: 160px;
    	height: 160px;
		top: 17px;
    	right: 6px;
		
	}
	// 60% {
	// 	width: 140px;
    // 	height: 140px;
		
	// }
	100% {
		width: 140px;
    	height: 140px;
		top: 20px;
    	right: 8px;
	}
	// 90% {
	// 	width: 140px;
    // 	height: 140px;
	// 	top: 20px;
    // 	right: 8px;
	// }
}



</style>
