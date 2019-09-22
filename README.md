Angular Particle:

1.	Create angular application
a.	Ng new <applicationName>
2.	In Index.html, include the particle script file
a.	  <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
3.	App.Component.html
a.	<div id="particles-js">
4.	Create a file particle-config.ts
export const ParticlesConfig = {
    particles: {
      number: {
        value: 70,
        density: {
          enable: true,
          value_area: 1400
        }
      },
      color: {
        value: '#283593'
      },
      shape: {
        type: 'polygon',
        stroke: {
          width: 1,
          color: '#283593'
        },
        polygon: {
          nb_sides: 6
        }
      },
      opacity: {
        value: 1,
        random: true,
        anim: {
          enable: true,
          speed: 0.8,
          opacity_min: 0.25,
          sync: true
        }
      },
      size: {
        value: 2,
        random: true,
        anim: {
          enable: true,
          speed: 10,
          size_min: 1.25,
          sync: true
        }
      },
      line_linked: {
        enable: true,
        distance: 150,
        color: '#283593',
        opacity: 1,
        width: 1
      },
      move: {
        enable: true,
        speed: 8,
        direction: 'none',
        random: true,
        straight: false,
        out_mode: 'out',
        bounce: true,
        attract: {
          enable: true,
          rotateX: 2000,
          rotateY: 2000
        }
      }
    },
    interactivity: {
      detect_on: 'canvas',
      events: {
        onhover: {
          enable: true,
          mode: 'grab'
        },
        onclick: {
          enable: true,
          mode: 'repulse'
        },
        resize: true
      },
      modes: {
        grab: {
          distance: 200,
          line_linked: {
            opacity: 3
          }
        },
        repulse: {
          distance: 250,
          duration: 2
        }
      }
    },
    retina_detect: true
}
5.	In AppComponent.ts, Implement the interface “OnInit” and place the below code:
a.	particlesJS('particles-js', ParticlesConfig, function() {});
b.	declare let particlesJS: any;
6. ng serve and open the browser