# Sine Drift 3D: Harmonic Retro Arcade Runner

> **Sine Drift 3D is a blazing-fast, fully autonomous 3D retro-arcade survival runner engineered entirely from mathematical first principles into a microscopic 3KB footprint!**

[![Budget](https://img.shields.io/badge/Byte%20Budget-%E2%89%A4%203072%20bytes-blue?style=for-the-badge)](dist/data_uri.txt)
[![Data URI Size](https://img.shields.io/badge/Data%20URI-3%2C069%20bytes-brightgreen?style=for-the-badge)](dist/data_uri.txt)
[![Raw HTML Size](https://img.shields.io/badge/Raw%20HTML-3%2C044%20bytes-green?style=for-the-badge)](dist/index.html)
[![Bites Badges](https://img.shields.io/badge/Hack%20Club%20Bites-%2B22%20BITES-orange?style=for-the-badge)](#-bites-badges-earned-22-bites-total)
[![Dependencies](https://img.shields.io/badge/Dependencies-Zero%20(Pure%20Vanilla)-purple?style=for-the-badge)](src/index.html)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

---

## 🌌 Project Overview (Judges & Demo Overview)

**Sine Drift 3D** is a fully functional, self-contained 3D retro arcade runner running with dynamic day/night cycles, procedural sound effects, different variety of enemy drones, and spinning collectible coins—all packaged directly inside a single **3KB executable Data URI**!

Drop into an endless hyperspace highway where the world around you is alive: an undulating trigonometric wireframe horizon bends dynamically beneath your ship as the sky cycles in real-time through a **dramatic Day/Night harmonic loop**—shifting from a blazing pale dawn with a radiant golden sun down into a starry neon twilight with a glowing lunar orb.

Dodge through waves of **autonomous patrolling hunter drones**, each locked into distinct lateral bounce vectors and dynamic speed tiers, while chasing down **spinning golden 3D perspective coins** that pulse and flip along the peaks of the sine waves. Backed by a **100% procedural Web Audio synthesizer**, every run pulses with a revving low-frequency engine hum, crystalline high-frequency collection chimes, and crunchy sawtooth impact crashes.

Pilot your delta-wing starfighter with razor-sharp precision: **drag your mouse left and right across the viewport** (or tap **A / D** and **Arrow Keys**) to bank across the ribbons, carve through the drone swarms, grab high-value coin drops, and rack up high scores on the live HUD—all running with zero external assets, zero textures, and zero libraries in pure vanilla Canvas!

---

## ⚡ The One-Line Data URI (Copy & Paste Into Any Browser)

Paste this entire line directly into the address bar of **Chrome**, **Edge**, **Firefox**, or **Safari** and press **Enter**:

```text
data:text/html,<body style=margin:0;overflow:hidden;background:black><canvas id=c></canvas><script>M=Math;R1=M.random;x=c.getContext('2d');A=0;k={};hi=t=z=W=0;V=[0,1.4,-1];B=_=>(R1()-.5)*220;S=[0,1,2,3];stX=S.map(R1);RC=_=>C={x:B(),z:400+R1()*300};R=_=>{st=1;go=sc=cn=px=tk=0;sp=.02;E=S.map(i=>({x:i*60-90,z:180+i*90,vx:V[i%3],k:i%3}));RC()};R();st=0;P=(f,y,v=.25,d=.2)=>{A&&(o=A.createOscillator(),g=A.createGain(),y&&(o.type=y),o.frequency.value=f,g.gain.value=v,g.gain.linearRampToValueAtTime(0,m=A.currentTime+d),o.connect(g).connect(A.destination),o.start(),o.stop(m))};onkeydown=onpointerdown=e=>{A?A.resume():A=new AudioContext;k[e.keyCode]=1;st&&!go||R()};onkeyup=e=>k[e.keyCode]=0;onpointermove=e=>e.buttons&&(px+=e.movementX);P3=(X,r)=>[W/2+X*(m=280/r),Y0+(26*M.sin(r*.03+t)*M.cos(X/67)+35)*m];J=(X,r,b)=>x[b?'moveTo':'lineTo'](...P3(X,r));T=(a,b,c,d)=>[b,a,tc,c,tc,d].map((v,i)=>i&1?x.fillText(v,W/2,Y0+i*22-55):x.fillStyle=v);L=_=>{t+=.03;z+=sp*20;dy=.5-.5*M.cos(t*.2);u=1-dy;tc='rgb('+[g=u*255|0,g,g]+')';cl='rgb('+[0,g,g/2+70|0]+')';cp='rgb('+[q=130+g/3|0,g/2|0,q]+')';if(st&&!go){tk++&3||(sc++,sp+=1e-5);px=M.max(-160,M.min(160,px+(k[68]|k[39]?6:k[65]|k[37]?-6:0)));tk&15||P(99+(tk*9&63),'triangle',.05)}W==innerWidth||(W=c.width=innerWidth,H=c.height=innerHeight,Y0=H/2-30,x.textAlign='center',x.font='18px monospace');x.fillStyle='rgb('+[q=255-g,q,q*.8|0]+')';x.fillRect(0,0,W,H);x.fillStyle='rgba(255,255,255,'+u+')';for(s of stX)x.fillRect(s*W,(s*Y0+t*4)%Y0,2,2);sY=Y0-60;x.shadowBlur=25;x.shadowColor=dy>.5?'orange':'gray';G=x.createRadialGradient(W/2,sY,0,W/2,sY,34);[0,1].map(j=>G.addColorStop(j,'rgb('+[j?70+150*dy|0:180+75*dy|0,j?60:160,(j?70:180)*u|0]+')'));x.fillStyle=G;x.beginPath();x.arc(W/2,sY,34,0,7);x.fill();x.shadowBlur=0;x.fillStyle=tc;x.fillText('SINE DRIFT',W/2,Y0-140);x.strokeStyle=cl;for(X=-160;X<161;X+=40){x.beginPath();for(Z=40,b=1;Z<1e3;Z+=30)(r=Z-z%30)>20&&(J(X,r,b),b=0);x.stroke()}x.strokeStyle=cp;for(Z=60;Z<1e3;Z+=80)if((r=Z-z%80)>20){x.beginPath();for(X=-160;X<161;X+=40)J(X,r,X==-160);x.stroke()}if(st){!go&&((C.z-=sp*22)<20||M.abs(C.z-65)<15&&M.abs(C.x-px)<25&&(cn++,sc+=50,P(1568),1))&&RC();C.z>20&&([p,q]=P3(C.x,C.z),x.fillStyle='gold',x.beginPath(),x.ellipse(p,q,M.sin(t*4)**2*(cr=3e3/C.z),cr,0,0,7),x.fill());E.map(e=>{!go&&(e.z-=sp*22,e.x+=e.vx,M.abs(e.x)>110&&(e.vx*=-1),e.z<20&&(e.z=550,e.x=B(),e.vx=V[e.k]),M.abs(e.z-68)<7&&M.abs(e.x-px)<24&&(go=1,sc>hi&&(hi=sc),P(99,'sawtooth')));e.z>20&&([p,q]=P3(e.x,e.z),d=3e3/e.z,x.fillStyle='rgb('+[255,e.k*60,e.k*120].map(v=>v*(.3+.7*dy)|0)+')',x.beginPath(),[-d,d].map(w=>(x.lineTo(p+w,q),x.lineTo(p,q+w))),x.fill())})}[sx,sy]=P3(px,65);x.fillStyle='gold';x.fillRect(sx-2,sy+4,4,4);x.strokeStyle='white';for(i of[-14,14])x.beginPath(),x.moveTo(sx,sy-15),x.lineTo(sx+i,sy+10),x.lineTo(sx,sy+3),x.fillStyle=go?'red':i<0?cl:'blue',x.fill(),x.stroke();!st&&x.strokeRect(W/2-85,Y0-8,170,74);K=`SC:${sc} CN:${cn} HI:${hi}`;!st||go?T(...go?['CRASH','red',K,'RETRY']:['','','DODGE DRONES','PLAY']):x.fillText(K,W/2,24);requestAnimationFrame(L)};L();</script></body>
```

---

## 🏆 Bites Badges Earned (+22 BITES Total)

| Badge | Criteria | Implementation | Points |
| :--- | :--- | :--- | :---: |
| **3D Rendering** | *Render in three dimensions. WebGL or something!* | True 3D perspective projection camera ($X \cdot \frac{280}{Z}, Y \cdot \frac{280}{Z}$), dynamic horizon depth clipping, undulating 3D sine-ribbon mesh, and perspective-scaled sprites. | **+8** |
| **Canvas API** | *Draw your app with the Canvas API.* | High-fps 2D Canvas vector rendering loop, procedural starfield, radial gradient suns, faceted geometric craft, and zero external DOM elements. | **+6** |
| **Web Audio API** | *Make sound with the Web Audio API. Synths, beeps, music.* | Pure procedural Web Audio synthesis featuring gain ramp envelopes, dynamic frequency sweeps, and multiple oscillator waveforms (`sine`, `triangle`, `sawtooth`). | **+5** |
| **Input Handling** | *Reacts to input: keyboard, mouse, touch, or mic.* | Multi-mode controls: `A` / `D` keys, `ArrowLeft` / `ArrowRight`, pointer/mouse dragging, touch swiping, and universal click-to-start. | **+3** |

---

## 🎮 Controls

| Action | Control |
| :--- | :--- |
| **Start / Retry** | Click screen, tap touch screen, or press any key / Space |
| **Navigate Left** | Drag mouse left, press `A`, or press `ArrowLeft` |
| **Navigate Right** | Drag mouse right, press `D`, or press `ArrowRight` |
| **Audio Start** | Automatically activates on your first click / keypress |

---

## 📐 Mathematical Architecture

### 1. Undulating Horizon Terrain
The ground surface undulates via a compound harmonic wave function:
$$Y(x, z, t) = 26 \cdot \sin(0.03 \cdot z + t) \cdot \cos\left(\frac{x}{67}\right) + 35$$

### 2. Perspective Camera Projection
World space coordinates $(X, Y, Z)$ map directly to 2D screen coordinates $(P_x, P_y)$ using a focal length multiplier of $280$:
$$P_x = \frac{W}{2} + X \cdot \frac{280}{Z}, \quad P_y = Y_0 + Y(x, z, t) \cdot \frac{280}{Z}$$

---

## 📂 Repository Structure

```
2/
├── .github/
│   └── workflows/
│       └── deploy.yml       # Automated GitHub Pages deployment
├── dist/
│   ├── index.html           # Minified standalone production build (3,044 bytes)
│   └── data_uri.txt         # Executable 1-line Data URI (3,069 bytes)
├── src/
│   └── index.html           # Full readable developer source code with comments
├── build.mjs                # Node.js build runner and byte budget verification
├── index.html               # GitHub Pages live web player
├── package.json             # NPM package scripts (build, test, dev)
├── .gitignore               # Clean git tracking rules
├── LICENSE                  # MIT Open Source License
└── README.md                # Documentation and Bites submission guide
```

---

## 🛠️ Development & Verification

```bash
# Verify byte budget (strictly <= 3,072 bytes)
npm run build

# Start local preview server on http://localhost:8080
npm run dev
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) - open source and free for demoscene, education, and hacking.
