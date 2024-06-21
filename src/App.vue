<template>
  <div id="container" style="background-color: black;">
    <div id="contact" style="z-index:15 ;width: 100%; display: flex; justify-content: end;">
      <a href="https://www.linkedin.com/in/ramon-larcher-b50806270/" style="font-family: monospace;transition: text-shadow 0.3s ease;text-decoration: none ;font-size: 20px ; padding-right:10px ;color: white; text-shadow:0px 0px 3px rgba(255, 255, 53, 1); ">Contact</a>
    </div>
    <div id="particles-js2" style="z-index: 6; position: absolute; width: 100%; height: 100vh"></div>

    <div id="div-topo" style="display: flex; flex-direction: row; align-items: center;justify-content: center;"> 
      <h1 id="titulo">
        <span id="hated">Hated </span>
        <span id="in">in </span>
        <span id="the">the </span>
        <span id="nation">Nation </span>
      </h1>
      <div id="bee1">
        <div ref="threeContainer" class="three-container"></div>
      </div>
    </div>

    <div id="first-text" style="display: flex; flex-direction: column; height: 100vh; align-items: center; justify-content:center; ">
      <p id="texto" style="color:white;">Hated in the Nation " é o sexto e último episódio da terceira temporada da série antológica britânica de ficção científica Black Mirror . Escrito pelo criador e showrunner da série Charlie Brooker e dirigido por James Hawes , estreou na Netflix em 21 de outubro de 2016, junto com o restante da terceira série. É o episódio mais longo de Black Mirror , com 89 minutos.Um episódio de inspiração nórdica noir ,<span style="background-color:rgb(157 157 39); color: black; "> "Hated in the Nation" segue os detetives Karin Parke ( Kelly Macdonald ) e Blue Coulson ( Faye Marsay ) enquanto eles investigam uma série de mortes visando os sujeitos do ódio nas redes sociais , nas mãos de Insetos Drones Autônomos</span>. (ADIs) que foram implantadas para combater catástrofes ambientais à medida que as abelhas estão próximas da extinção. Foi filmado principalmente em Londres.Baseado na experiência de Brooker ao receber cartas de ódio depois de escrever uma coluna no Guardian em 2004 que menosprezava George W. Bush , o episódio foi comparado com Arquivo X e explorou temas como vigilância governamental e ambientalismo.</p>
      <div id="bee2" style="display: flex; align-items: center; justify-content: center; margin-top: 10px; z-index: 10;">
        <div ref="threeContainer2" class="three-container2"></div>
      </div>
      <div id="particles-js" style="position: absolute; width: 100%; height: 100vh; z-index: 0;"></div>

    </div>


  </div>
</template>
<script>
import * as THREE from 'three';
import ScrollReveal from 'scrollreveal';
import 'particles.js';
import { onMounted, nextTick } from 'vue';

import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls.js';
import { PointLight } from 'three';
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';

export default {
  setup() {
    onMounted(() => {
      nextTick(() => {
        window.particlesJS('particles-js',{
          "particles": {
            "number": {
              "value": 80,
              "density": {
                "enable": true,
                "value_area": 800
              }
            },
            "color": {
              "value": "#ffffff"
            },
            "shape": {
              "type": "circle",
              "stroke": {
                "width": 0,
                "color": "#000000"
              },
              "polygon": {
                "nb_sides": 5
              },
              "image": {
                "src": "img/github.svg",
                "width": 100,
                "height": 100
              }
            },
            "opacity": {
              "value": 0.5,
              "random": false,
              "anim": {
                "enable": false,
                "speed": 1,
                "opacity_min": 0.1,
                "sync": false
              }
            },
            "size": {
              "value": 3,
              "random": true,
              "anim": {
                "enable": false,
                "speed": 40,
                "size_min": 0.1,
                "sync": false
              }
            },
            "line_linked": {
              "enable": true,
              "distance": 150,
              "color": "#ffffff",
              "opacity": 0.4,
              "width": 1
            },
            "move": {
              "enable": true,
              "speed": 6,
              "direction": "none",
              "random": false,
              "straight": false,
              "out_mode": "out",
              "bounce": false,
              "attract": {
                "enable": false,
                "rotateX": 600,
                "rotateY": 1200
              }
            }
          },
          "interactivity": {
            "detect_on": "canvas",
            "events": {
              "onhover": {
                "enable": true,
                "mode": "repulse"
              },
              "onclick": {
                "enable": true,
                "mode": "push"
              },
              "resize": true
            },
            "modes": {
              "grab": {
                "distance": 400,
                "line_linked": {
                  "opacity": 1
                }
              },
              "bubble": {
                "distance": 400,
                "size": 40,
                "duration": 2,
                "opacity": 8,
                "speed": 3
              },
              "repulse": {
                "distance": 200,
                "duration": 0.4
              },
              "push": {
                "particles_nb": 4
              },
              "remove": {
                "particles_nb": 2
              }
            }
          },
          "retina_detect": true
        });

        window.particlesJS('particles-js2',{
          "particles": {
            "number": {
              "value": 80,
              "density": {
                "enable": true,
                "value_area": 800
              }
            },
            "color": {
              "value": "#ffffff"
            },
            "shape": {
              "type": "circle",
              "stroke": {
                "width": 0,
                "color": "#000000"
              },
              "polygon": {
                "nb_sides": 5
              },
              "image": {
                "src": "img/github.svg",
                "width": 100,
                "height": 100
              }
            },
            "opacity": {
              "value": 0.5,
              "random": false,
              "anim": {
                "enable": false,
                "speed": 1,
                "opacity_min": 0.1,
                "sync": false
              }
            },
            "size": {
              "value": 3,
              "random": true,
              "anim": {
                "enable": false,
                "speed": 40,
                "size_min": 0.1,
                "sync": false
              }
            },
            "line_linked": {
              "enable": true,
              "distance": 150,
              "color": "#ffffff",
              "opacity": 0.4,
              "width": 1
            },
            "move": {
              "enable": true,
              "speed": 6,
              "direction": "none",
              "random": false,
              "straight": false,
              "out_mode": "out",
              "bounce": false,
              "attract": {
                "enable": false,
                "rotateX": 600,
                "rotateY": 1200
              }
            }
          },
          "interactivity": {
            "detect_on": "canvas",
            "events": {
              "onhover": {
                "enable": true,
                "mode": "repulse"
              },
              "onclick": {
                "enable": true,
                "mode": "push"
              },
              "resize": true
            },
            "modes": {
              "grab": {
                "distance": 400,
                "line_linked": {
                  "opacity": 1
                }
              },
              "bubble": {
                "distance": 400,
                "size": 40,
                "duration": 2,
                "opacity": 8,
                "speed": 3
              },
              "repulse": {
                "distance": 200,
                "duration": 0.4
              },
              "push": {
                "particles_nb": 4
              },
              "remove": {
                "particles_nb": 2
              }
            }
          },
          "retina_detect": true
        });
      
      });
    });
  
  },
  name: 'ThreeComponent',
  mounted() {
   
    const sr = ScrollReveal();

    const container = this.$refs.threeContainer;
    if (!container) {
      console.error('Element with ref "threeContainer" not found');
      return;
    }
    const renderer = new THREE.WebGLRenderer({ alpha: true });

    renderer.setSize(200, 200);
    container.appendChild(renderer.domElement);

    const scene = new THREE.Scene();
    scene.background = null;

    const camera = new THREE.PerspectiveCamera(45, 1, 1, 3000);
    camera.rotation.y = Math.PI;
    camera.position.x = 800;
    camera.position.y = 100;
    camera.position.z = 1000;

    const controls = new OrbitControls(camera, renderer.domElement);
    controls.update();

    const light1 = new PointLight(0xc4c4c4, 500000);
    light1.position.set(0, 300, 500);
    scene.add(light1);

    const light2 = new PointLight(0xc4c4c4, 500000);
    light2.position.set(500, 100, 0);
    scene.add(light2);

    const light3 = new PointLight(0xc4c4c4, 500000);
    light3.position.set(0, 100, -500);
    scene.add(light3);

    const light4 = new PointLight(0xc4c4c4, 50000);
    light4.position.set(-500, 300, 500);
    scene.add(light4);

    const gltfLoader = new GLTFLoader();
    gltfLoader.load('/assets/bee_gltf.glb', (gltf) => {
      const model = gltf.scene;
      model.scale.set(600, 600, 600);
      model.position.y = -50;
      scene.add(model);

      if (gltf.animations && gltf.animations.length > 0) {
        const mixer = new THREE.AnimationMixer(model);
        gltf.animations.forEach((clip) => {
          mixer.clipAction(clip).play();
        });

        const animate = () => {
          requestAnimationFrame(animate);
          controls.update();
          mixer.update(0.01);
          renderer.render(scene, camera);
        };

        animate();
      } else {
        console.log('Nenhuma animação encontrada no modelo.');
      }
    });

    //BEE2
    const container2 = this.$refs.threeContainer2;

    const renderer2 = new THREE.WebGLRenderer({ alpha: true });

    renderer2.setSize(330, 300);
    container2.appendChild(renderer2.domElement);

    const scene2 = new THREE.Scene();
    scene.background = null;

    const camera2 = new THREE.PerspectiveCamera(45, 1, 1, 3000);
    camera2.rotation.y = Math.PI;
    camera2.position.x = -1700;
    camera2.position.y = 500;
    camera2.position.z = 1000;

    const controls2 = new OrbitControls(camera2, renderer2.domElement);
    controls2.update();

    const bee2light1 = new PointLight(0xc4c4c4, 800000);
    bee2light1.position.set(0, 300, 500);
    scene2.add(bee2light1);

    const bee2light2 = new PointLight(0xc4c4c4, 800000);
    bee2light2.position.set(500, 100, 0);
    scene2.add(bee2light2);

    const bee2light3 = new PointLight(0xc4c4c4, 800000);
    bee2light3.position.set(0, 100, -500);
    scene2.add(bee2light3);

    const bee2light4 = new PointLight(0xc4c4c4, 80000);
    bee2light4.position.set(-500, 300, 500);
    scene2.add(bee2light4);

    const gltfLoader2 = new GLTFLoader();
    gltfLoader2.load('/assets/bee1.glb', (gltf) => {
      const model = gltf.scene;
      model.scale.set(300, 300, 300);
      model.position.y = -50;
      scene2.add(model);

      if (gltf.animations && gltf.animations.length > 0) {
        const mixer = new THREE.AnimationMixer(model);
        gltf.animations.forEach((clip) => {
          mixer.clipAction(clip).play();
        });

        const animate = () => {
          requestAnimationFrame(animate);
          controls2.update();
          mixer.update(0.01);
          renderer2.render(scene2, camera2);
        };

        animate();
      } else {
        console.log('Nenhuma animação encontrada no modelo.');
      }
    });



    const animateSpan = (id) => {

      const span = document.querySelector("#"+id)
      //texto original sem modificações 
      const textSpan = span.textContent;
      if(id == 'hated'){
        const typesSpan = ['Hated','H ted','Ha ed','Hat d']
        let indiceSorteado = Math.floor(Math.random() * typesSpan.length);
        let elementoSorteado = typesSpan[indiceSorteado];

        span.textContent = elementoSorteado+' '
        span.style.setProperty('text-shadow', 'rgb(255, 255, 53) 0px 0px 8px', 'important');

      }else if(id == 'nation'){
        const typesSpan = ['N tion','Na ion','Nat on','Nati n']
        let indiceSorteado = Math.floor(Math.random() * typesSpan.length);
        let elementoSorteado = typesSpan[indiceSorteado];

        span.textContent = elementoSorteado+' '
        span.style.setProperty('text-shadow', 'rgb(255, 255, 53) 0px 0px 8px', 'important');

      }
      //voltar com o texto original
      setTimeout(()=>{
        span.textContent =  textSpan + " ";
        span.style.setProperty('text-shadow', 'rgb(255, 255, 53) 0px 0px 13px', 'important');
      },300)
    }

    const animateNeon = () => {
      
      //array de spans (palavras) que serao animados(as)
      const spans = ['hated','nation'];

      setInterval(() => {
          //sortear spans que serao animados
          let indiceSorteado = Math.floor(Math.random() * spans.length);
          let elementoSorteado = spans[indiceSorteado];
          animateSpan(elementoSorteado)
      }, 8000);
    };

    animateNeon()

    sr.reveal('#div-topo',{
        duration: 8000,
        dalay:800,
        origin: 'left',
        distance: '1000px',
        easing: 'ease-out',
        mobile: true,
      });
    sr.reveal('#bee1',{
      duration:20000,
      dalay:1000,
      origin: 'top',
      distance: '1000px',
      easing: 'ease-out',
      mobile: true,
    });
    sr.reveal('#texto',{
      duration: 5000,
      dalay:500,
      origin: 'left',
      distance: '800px',
      easing: 'ease-out',
      mobile: true,
    });
    sr.reveal('#bee2',{
      duration: 15000,
      dalay:4000,
      origin: 'right',
      easing: 'ease-out',
      mobile: true,
    });
  }
};
</script>
<style scoped>

.three-container {
  width: 200px;
  height: 200px;
}
.three-container2 {
  width: 200px;
  height: 200px;
  display: flex;
  align-items: center; justify-content:center; 
}
#container{
  width: 100%;
  display: flex;
  flex-direction: column;
}
#div-topo{
  z-index: 10;
  visibility: hidden;
  height: 100vh;
}

#titulo {
  font-family: monospace; 
  font-size: 60px;
  color: white;
}

#titulo span {
  text-shadow: 0px 0px 13px rgba(255, 255, 53, 1);
  color: #ffffec;
}
#bee2{
  visibility: hidden;
}
#bee1{
  visibility: hidden;
}
#first-text{
  display: flex;
  z-index: 0;
  font-size: 30px;
  padding: 30px;
  align-items: center;
  justify-content: center;
}

#contact>a:hover{
  text-shadow: 0px 0px 20px rgba(255, 255, 53, 1) !important;
}


@media only screen and (max-width: 800px) {
  #div-topo {
    flex-direction: column-reverse !important;
  }
  #first-text{
    font-size: 20px;
  }
  #titulo{
    padding-left: 20px;
  }
  #particles-js2{
    z-index: 0 !important;
  }
}
</style>