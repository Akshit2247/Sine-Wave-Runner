# 🚀 Sine Drift 3D

> **A full 3D retro arcade runner that fits inside a single 3KB bookmark.** No downloads, zero libraries, zero external image assets—just pure math, canvas drawing, and real-time audio synthesis.

[![Live Size](https://img.shields.io/badge/Data%20URI-3%2C069%20bytes-brightgreen?style=flat-square)](dist/data_uri.txt)
[![Byte Budget](https://img.shields.io/badge/Budget-%E2%89%A4%203%2C072%20bytes-blue?style=flat-square)](dist/data_uri.txt)
[![Hack Club Bites](https://img.shields.io/badge/Hack%20Club%20Bites-%2B22%20Points-orange?style=flat-square)](#-hack-club-bites-breakdown-22-points)
[![Tech](https://img.shields.io/badge/Built%20With-Canvas%20%2B%20WebAudio-purple?style=flat-square)](src/index.html)
[![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)](LICENSE)

---

## 🕹️ Try it right now (Copy & Paste)

You don't need to clone this repo or install anything. Just copy this line, paste it into your browser's address bar (Chrome, Edge, Firefox, or Safari), and press **Enter**:

```text
data:text/html,<body style=margin:0;overflow:hidden;background:black><canvas id=c></canvas><script>M=Math;R1=M.random;x=c.getContext('2d');A=0;k={};hi=t=z=W=0;V=[0,1.4,-1];B=_=>(R1()-.5)*220;S=[0,1,2,3];stX=S.map(R1);RC=_=>C={x:B(),z:400+R1()*300};R=_=>{st=1;go=sc=cn=px=tk=0;sp=.02;E=S.map(i=>({x:i*60-90,z:180+i*90,vx:V[i%3],k:i%3}));RC()};R();st=0;P=(f,y,v=.25,d=.2)=>{A&&(o=A.createOscillator(),g=A.createGain(),y&&(o.type=y),o.frequency.value=f,g.gain.value=v,g.gain.linearRampToValueAtTime(0,m=A.currentTime+d),o.connect(g).connect(A.destination),o.start(),o.stop(m))};onkeydown=onpointerdown=e=>{A?A.resume():A=new AudioContext;k[e.keyCode]=1;st&&!go||R()};onkeyup=e=>k[e.keyCode]=0;onpointermove=e=>e.buttons&&(px+=e.movementX);P3=(X,r)=>[W/2+X*(m=280/r),Y0+(26*M.sin(r*.03+t)*M.cos(X/67)+35)*m];J=(X,r,b)=>x[b?'moveTo':'lineTo'](...P3(X,r));T=(a,b,c,d)=>(!a&&x.strokeRect(W/2-85,Y0-18,170,66),[a,c,d].map((v,i)=>(x.fillStyle=i?tc:b,x.fillText(v,W/2,Y0+i*33-33))));L=_=>{t+=.03;z+=sp*20;dy=.5-.5*M.cos(t*.2);u=1-dy;tc='rgb('+[g=u*255|0,g,g]+')';cl='rgb('+[0,g,g/2+70|0]+')';cp='rgb('+[q=130+g/3|0,g/2|0,q]+')';if(st&&!go){tk++&3||sc++;sp=.02+sc/12e4;px=M.max(-160,M.min(160,px+(k[68]|k[39]?6:k[65]|k[37]?-6:0)));tk&15||P(99+(tk*9&63),'triangle',.05)}W==innerWidth||(W=c.width=innerWidth,H=c.height=innerHeight,Y0=H/2-30,x.textAlign='center',x.font='18px monospace');x.fillStyle='rgb('+[q=255-g,q,q*.8|0]+')';x.fillRect(0,0,W,H);x.fillStyle='rgba(255,255,255,'+u+')';for(s of stX)x.fillRect(s*W,(s*Y0+t*4)%25Y0,2,2);sY=Y0-60;x.shadowBlur=25;x.shadowColor=dy>.5?'gold':'gray';G=x.createRadialGradient(W/2,sY,0,W/2,sY,34);[0,1].map(j=>G.addColorStop(j,'rgb('+[j?70+150*dy|0:180+75*dy|0,j?60:160,(j?70:180)*u|0]+')'));x.fillStyle=G;x.beginPath();x.arc(W/2,sY,34,0,7);x.fill();x.shadowBlur=0;x.fillStyle=tc;x.fillText('SINE DRIFT',W/2,Y0-140);x.strokeStyle=cl;for(X=-160;X<161;X+=40){x.beginPath();for(Z=40;Z<1e3;Z+=30)(r=Z-z%2530)>20&&J(X,r,Z==40);x.stroke()}x.strokeStyle=cp;for(Z=60;Z<1e3;Z+=80)if((r=Z-z%2580)>20){x.beginPath();for(X=-160;X<161;X+=40)J(X,r,X==-160);x.stroke()}if(st){!go&&((C.z-=sp*22)<20||M.abs(C.z-65)<15&&M.abs(C.x-px)<25&&(cn++,sc+=50,P(1568),1))&&RC();C.z>20&&([p,q]=P3(C.x,C.z),x.fillStyle='gold',x.beginPath(),x.ellipse(p,q,M.sin(t*4)**2*(cr=3360/C.z),cr,0,0,7),x.fill());E.map(e=>{!go&&(e.z-=sp*22,e.x+=e.vx,M.abs(e.x)>110&&(e.vx*=-1),e.z<20&&(e.z=550,e.x=B(),e.vx=V[e.k]),M.abs(e.z-68)<7&&M.abs(e.x-px)<24&&(go=1,sc>hi&&(hi=sc),P(99,'sawtooth')));e.z>20&&([p,q]=P3(e.x,e.z),d=3640/e.z,x.fillStyle='rgb('+[255,e.k*60,e.k*120].map(v=>v*(.3+.7*dy)|0)+')',x.beginPath(),[-d,d].map(w=>(x.lineTo(p+w,q),x.lineTo(p,q+w))),x.fill())})}[sx,sy]=P3(px,65);x.fillStyle='gold',x.fillRect(sx-2,sy+4,4,4);x.strokeStyle='white';for(i of[-14,14])x.beginPath(),x.moveTo(sx,sy-15),x.lineTo(sx+i,sy+10),x.lineTo(sx,sy+3),x.fillStyle=go?'red':i<0?cl:'blue',x.fill(),x.stroke();K=`SC:${sc} CN:${cn} HI:${hi}`;!st||go?T(...go?['CRASH','red',K,'RETRY']:['','','DODGE DRONES','PLAY']):x.fillText(K,W/2,24);requestAnimationFrame(L)};L();</script></body>
```

---

## 💡 What is this project?

The challenge was simple: **Build an entire, playable, audiovisual 3D game that fits under 3,072 bytes (3KB) as a self-contained Data URI.**

Normally, modern web games require megabytes of images, sound files, Webpack bundles, and physics engines. Here, every visual element, sound wave, and mathematical curve is generated on the fly in real-time JavaScript:

- **An Undulating 3D Wireframe Ground:** Instead of flat polygons, the track is a mathematical sine-wave grid that ripples as you fly forward.
- **Dynamic Day / Night Cycle:** The game seamlessly shifts from pale daylight with a glowing orange sun down into a starry neon midnight with a silver moon.
- **Synthesized Audio:** Built with the browser's Web Audio API. You get an accelerating low-end engine hum, crisp musical chimes when you grab coins, and a crunching bass-decay crash sound.
- **Roaming Drones & Collectibles:** Obstacle drones roam back and forth across different lanes, while 3D perspective-flipping golden coins reward you with bonus points.
- **Controls That Actually Feel Good:** Play with **A / D**, the **Arrow Keys**, or by **clicking and dragging your mouse** across the screen.

---

## 🎮 How to Play

| Goal | Instructions |
| :--- | :--- |
| **Start / Retry** | Click anywhere on the screen or press any key |
| **Steer Ship** | Drag your mouse left/right, press **A / D**, or use the **Arrow Keys** |
| **Collect Coins** | Fly directly into spinning gold coins (+50 points each) |
| **Dodge Drones** | Stay clear of incoming colored hunter drones |
| **Audio** | Sound starts automatically on your first click/keypress |

---

## 🏆 Hack Club Bites Breakdown (+22 Points)

| Challenge | Points | What was built |
| :--- | :---: | :--- |
| **3D Rendering** | **+8** | A custom 3D perspective camera engine ($X \cdot \frac{280}{Z}, Y \cdot \frac{280}{Z}$) calculating depth, dynamic horizon clipping, and undulating terrain in real-time. |
| **Canvas API** | **+6** | 60 FPS HTML5 Canvas vector rendering loop featuring radial gradient suns, a procedural starfield, and 3D delta-wing crafts. |
| **Web Audio API** | **+5** | Pure procedural synthesizer using oscillator nodes and gain ramps (triangle wave engine, sine wave coin pings at 1568Hz, sawtooth crash crunch at 99Hz). |
| **Input Handling** | **+3** | Multi-modal controls: responsive keyboard input (A/D & Arrows), pointer/mouse drag navigation (`movementX`), touch, and universal restart. |

---

## 🧠 The Math Behind the Game

How do you make a 3D landscape in just a few lines of code?

### 1. The Sine Wave Terrain
The ground isn't a pre-made 3D model; it's calculated live for every single grid vertex:
$$Y(x, z, t) = 26 \cdot \sin(0.03 \cdot z + t) \cdot \cos\left(\frac{x}{67}\right) + 35$$

### 2. The 3D Camera Projection
World coordinates $(X, Y, Z)$ get mapped to your 2D screen using perspective division:
$$P_x = \frac{\text{Width}}{2} + X \cdot \frac{280}{Z}, \quad P_y = \text{Horizon} + Y \cdot \frac{280}{Z}$$

### 3. The Day / Night Harmonic Cycle
Sky brightness, wireframe colors, and celestial gradients shift smoothly with time:
$$\Delta y = 0.5 - 0.5 \cdot \cos(t \cdot 0.2)$$

---

## 📁 Repository Structure

```text
2/
├── .github/
│   └── workflows/
│       └── deploy.yml       # Automatic GitHub Pages deployment
├── dist/
│   ├── index.html           # Minified production build (3,044 bytes)
│   └── data_uri.txt         # Executable 1-line Data URI (3,069 bytes)
├── src/
│   └── index.html           # Fully readable, well-commented developer source
├── build.mjs                # Size verification & syntax testing script
├── index.html               # Web launcher for instant browser play
├── package.json             # NPM scripts (build, test, dev)
├── LICENSE                  # MIT License
└── README.md                # Project documentation
```

---

## 🛠️ Local Development & Testing

Want to check the byte size or run the game locally?

```bash
# 1. Run the build script to verify the byte budget (must be <= 3,072 bytes)
npm run build

# 2. Start a local preview server on http://localhost:8080
npm run dev
```

### Build Verification Output
```text
========================================================
         SINE DRIFT 3D - BUILD & SIZE REPORT         
========================================================
 Budget Limit:           3072 bytes
 Raw HTML Size:          3044 bytes (28 bytes remaining)
 Data URI Size:          3069 bytes (3 bytes remaining)
 JavaScript Syntax:      VALID [PASS]
 Raw Under Budget:       [PASS]
 URI Under Budget:       [PASS]
--------------------------------------------------------
 OVERALL RESULT:         SUCCESS - READY FOR BITES (+22 BITES)
========================================================
```

---

## 📜 License

MIT License — free to inspect, play, learn from, and modify.
