```aura width=800 height=440
<div style={{ position:'relative', display:'flex', flexDirection:'column', alignItems:'center', justifyContent:'center', width:'100%', height:'100%', padding:'34px 44px', background:'#100C17', border:'1px solid #2B2537', borderRadius:24, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <style>{`
    @keyframes starPulse { 0%,100% { opacity:.18 } 50% { opacity:.75 } }
    @keyframes floatDiamond { 0%,100% { transform:translate(0,0) rotate(45deg) } 50% { transform:translate(0,12px) rotate(62deg) } }
    @keyframes floatCircle { 0%,100% { transform:translate(0,0) } 50% { transform:translate(-10px,8px) } }
    @keyframes sparkle { 0%,100% { opacity:.45; transform:scale(.85) } 50% { opacity:1; transform:scale(1.1) } }
    #hero-stars-a { animation:starPulse 3.8s ease-in-out infinite; }
    #hero-stars-b { animation:starPulse 5.2s ease-in-out infinite 1.1s; }
    #hero-diamond { transform-origin:130px 110px; animation:floatDiamond 13s ease-in-out infinite; }
    #hero-circle { animation:floatCircle 11s ease-in-out infinite; }
    #hero-sparkle { transform-origin:400px 70px; animation:sparkle 3s ease-in-out infinite; }
  `}</style>

  <svg width="800" height="440" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="heroGoldGlow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(238,179,43,.16)" />
        <stop offset="100%" stopColor="rgba(238,179,43,0)" />
      </radialGradient>
      <radialGradient id="heroLavGlow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(117,82,148,.18)" />
        <stop offset="100%" stopColor="rgba(117,82,148,0)" />
      </radialGradient>
      <linearGradient id="heroFadeLine" x1="0" x2="1">
        <stop offset="0%" stopColor="rgba(238,179,43,0)" />
        <stop offset="50%" stopColor="rgba(238,179,43,.7)" />
        <stop offset="100%" stopColor="rgba(238,179,43,0)" />
      </linearGradient>
    </defs>

    <ellipse cx="400" cy="220" rx="360" ry="260" fill="url(#heroGoldGlow)" />
    <ellipse cx="100" cy="410" rx="260" ry="180" fill="url(#heroLavGlow)" />
    <ellipse cx="760" cy="40" rx="230" ry="160" fill="url(#heroLavGlow)" />

    <g id="hero-stars-a" fill="#EEB32B">
      <circle cx="72" cy="76" r="1.4"/><circle cx="176" cy="48" r="1.1"/><circle cx="265" cy="102" r="1.2"/>
      <circle cx="612" cy="66" r="1.2"/><circle cx="714" cy="126" r="1.5"/><circle cx="744" cy="330" r="1.1"/>
      <circle cx="120" cy="324" r="1.2"/><circle cx="215" cy="380" r="1.1"/><circle cx="554" cy="392" r="1.3"/>
    </g>
    <g id="hero-stars-b" fill="#EDEBEF">
      <circle cx="108" cy="188" r="1"/><circle cx="328" cy="58" r="1"/><circle cx="462" cy="90" r="1.1"/>
      <circle cx="670" cy="236" r="1"/><circle cx="72" cy="280" r="1"/><circle cx="348" cy="402" r="1"/>
      <circle cx="620" cy="354" r="1"/><circle cx="758" cy="210" r="1"/>
    </g>

    <rect id="hero-diamond" x="86" y="66" width="88" height="88" fill="none" stroke="rgba(238,179,43,.11)" />
    <circle id="hero-circle" cx="690" cy="105" r="54" fill="none" stroke="rgba(238,179,43,.10)" />
    <path d="M575 347 L620 390 L530 390 Z" fill="none" stroke="rgba(238,179,43,.08)" />

    <g id="hero-sparkle" stroke="#EEB32B" strokeWidth="1.5">
      <path d="M400 58 V82 M388 70 H412" />
      <path d="M393 63 L407 77 M407 63 L393 77" opacity=".45" />
    </g>
    <path d="M230 350 H570" stroke="url(#heroFadeLine)" strokeWidth="1" />
  </svg>

  <div style={{ display:'flex', flexDirection:'column', alignItems:'center', textAlign:'center' }}>
    <span style={{ fontSize:15, fontWeight:700, color:'#EEB32B', letterSpacing:3.2, textTransform:'uppercase' }}>Software Engineer Intern @ Google</span>
    <span style={{ marginTop:16, fontSize:67, fontWeight:800, color:'#FFFFFF', letterSpacing:-3.1, lineHeight:.98 }}>Heba Alazzeh</span>
    <span style={{ marginTop:17, fontSize:15, color:'rgba(237,235,239,.72)', letterSpacing:.2 }}>UC Berkeley Computer Science &nbsp;•&nbsp; AI Research @ Stanford</span>

    <div style={{ display:'flex', gap:8, marginTop:27 }}>
      {['GOOGLE CLOUD SDK','STANFORD SISL + MINERAL-X','MTC BERKELEY'].map((label, i) => (
        <span key={label} style={{ padding:'7px 11px', borderRadius:999, background:i===0 ? '#EEB32B' : 'rgba(255,255,255,.035)', border:i===0 ? '1px solid #EEB32B' : '1px solid #2B2537', color:i===0 ? '#100C17' : 'rgba(237,235,239,.72)', fontSize:9.5, fontWeight:750, letterSpacing:1.2 }}>{label}</span>
      ))}
    </div>
  </div>

  <span style={{ position:'absolute', bottom:21, fontSize:9.5, color:'rgba(237,235,239,.30)', letterSpacing:2.1, textTransform:'uppercase' }}>software · research · community</span>
</div>
```

```aura width=800 height=285
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 30px', background:'#171320', border:'1px solid #2B2537', borderRadius:20, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:14 }}>
    <svg width="88" height="22"><path d="M0 11 Q11 0 22 11 T44 11 T66 11 T88 11" fill="none" stroke="#EEB32B" strokeWidth="1" opacity=".32"/><path d="M0 11 Q11 22 22 11 T44 11 T66 11 T88 11" fill="none" stroke="#EEB32B" strokeWidth="1" opacity=".32"/><circle cx="44" cy="11" r="3" fill="#EEB32B" opacity=".45"/></svg>
    <span style={{ fontSize:23, fontWeight:800, color:'#EDEBEF', letterSpacing:-.6 }}>About</span>
    <svg width="88" height="22"><path d="M0 11 Q11 0 22 11 T44 11 T66 11 T88 11" fill="none" stroke="#EEB32B" strokeWidth="1" opacity=".32"/><path d="M0 11 Q11 22 22 11 T44 11 T66 11 T88 11" fill="none" stroke="#EEB32B" strokeWidth="1" opacity=".32"/><circle cx="44" cy="11" r="3" fill="#EEB32B" opacity=".45"/></svg>
  </div>
  <div style={{ width:70, height:1, margin:'9px auto 0', background:'#EEB32B', opacity:.7 }}></div>

  <div style={{ display:'flex', gap:18, flex:1, marginTop:21 }}>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'18px 21px', background:'#100C17', border:'1px solid #2B2537', borderRadius:15 }}>
      <span style={{ fontSize:19, fontWeight:750, color:'#EDEBEF', lineHeight:1.32 }}>I like building technology that moves beyond the demo and actually helps people.</span>
      <span style={{ marginTop:13, fontSize:12.5, color:'#968FA3', lineHeight:1.62 }}>My work sits across software engineering, AI research, and community building — with a focus on accessible, ethical systems and sharing opportunities instead of gatekeeping them.</span>
    </div>
    <div style={{ display:'flex', flexDirection:'column', gap:9, width:235 }}>
      {[
        ['NOW','SWE Intern @ Google'],
        ['STUDYING','CS @ UC Berkeley'],
        ['RESEARCH','AI @ Stanford'],
        ['BUILDING','MTC @ Berkeley']
      ].map((x, i) => (
        <div key={x[0]} style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'10px 14px', background:i===0 ? 'rgba(238,179,43,.08)' : '#100C17', border:i===0 ? '1px solid rgba(238,179,43,.38)' : '1px solid #2B2537', borderRadius:12 }}>
          <span style={{ fontSize:8.5, color:i===0 ? '#EEB32B' : '#968FA3', letterSpacing:1.7 }}>{x[0]}</span>
          <span style={{ marginTop:3, fontSize:12.5, fontWeight:700, color:'#EDEBEF' }}>{x[1]}</span>
        </div>
      ))}
    </div>
  </div>
</div>
```

```aura width=800 height=350
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 28px', background:'#100C17', border:'1px solid #2B2537', borderRadius:20, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:14 }}>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
    <span style={{ fontSize:23, fontWeight:800, color:'#EDEBEF' }}>Experience</span>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
  </div>
  <div style={{ width:70, height:1, margin:'9px auto 0', background:'#EEB32B', opacity:.7 }}></div>

  <div style={{ display:'flex', gap:13, flex:1, marginTop:21 }}>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'space-between', width:470, padding:'22px 23px', background:'#171320', border:'1px solid rgba(238,179,43,.38)', borderRadius:16 }}>
      <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
        <span style={{ padding:'5px 9px', borderRadius:999, background:'#EEB32B', color:'#100C17', fontSize:8.5, fontWeight:800, letterSpacing:1.4 }}>CURRENT</span>
        <span style={{ fontSize:9, color:'#968FA3', letterSpacing:1.4 }}>SUMMER 2026</span>
      </div>
      <div style={{ display:'flex', flexDirection:'column' }}>
        <span style={{ fontSize:16, fontWeight:700, color:'#EEB32B' }}>GOOGLE</span>
        <span style={{ marginTop:5, fontSize:28, fontWeight:800, color:'#EDEBEF', letterSpacing:-.8 }}>Software Engineer Intern</span>
        <span style={{ marginTop:9, fontSize:12, color:'#968FA3', lineHeight:1.55 }}>Cloud SDK · Python SDK performance & architectural optimization</span>
      </div>
      <span style={{ fontSize:10, color:'rgba(237,235,239,.35)', letterSpacing:1.25 }}>SAN FRANCISCO BAY AREA</span>
    </div>

    <div style={{ display:'flex', flexDirection:'column', gap:13, flex:1 }}>
      <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'17px', background:'#171320', border:'1px solid #2B2537', borderRadius:16 }}>
        <span style={{ fontSize:8.5, color:'#968FA3', letterSpacing:1.5 }}>PREVIOUS</span>
        <span style={{ marginTop:7, fontSize:19, fontWeight:780, color:'#EDEBEF' }}>Uber</span>
        <span style={{ marginTop:4, fontSize:11, color:'#968FA3' }}>software engineering</span>
      </div>
      <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'17px', background:'#171320', border:'1px solid #2B2537', borderRadius:16 }}>
        <span style={{ fontSize:8.5, color:'#968FA3', letterSpacing:1.5 }}>PREVIOUS</span>
        <span style={{ marginTop:7, fontSize:19, fontWeight:780, color:'#EDEBEF' }}>Snap Inc.</span>
        <span style={{ marginTop:4, fontSize:11, color:'#968FA3' }}>augmented reality · engineering</span>
      </div>
    </div>
  </div>
</div>
```

```aura width=800 height=310
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 28px', background:'#171320', border:'1px solid #2B2537', borderRadius:20, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:14 }}>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
    <span style={{ fontSize:23, fontWeight:800, color:'#EDEBEF' }}>Research</span>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
  </div>
  <div style={{ width:70, height:1, margin:'9px auto 0', background:'#EEB32B', opacity:.7 }}></div>

  <div style={{ display:'flex', gap:13, flex:1, marginTop:21 }}>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'space-between', flex:1, padding:'20px', background:'#100C17', border:'1px solid #2B2537', borderRadius:16 }}>
      <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
        <span style={{ fontSize:9, fontWeight:800, color:'#EEB32B', letterSpacing:1.7 }}>STANFORD SISL</span>
        <span style={{ fontSize:17, color:'#EEB32B' }}>✦</span>
      </div>
      <span style={{ marginTop:15, fontSize:19, fontWeight:760, color:'#EDEBEF', lineHeight:1.25 }}>Autonomous systems & human-centered AI</span>
      <span style={{ marginTop:10, fontSize:11.5, color:'#968FA3', lineHeight:1.5 }}>Research on intelligent systems that can reason, adapt, and operate in real-world environments.</span>
    </div>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'space-between', flex:1, padding:'20px', background:'#100C17', border:'1px solid #2B2537', borderRadius:16 }}>
      <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
        <span style={{ fontSize:9, fontWeight:800, color:'#EEB32B', letterSpacing:1.7 }}>STANFORD MINERAL-X</span>
        <span style={{ fontSize:17, color:'#EEB32B' }}>◇</span>
      </div>
      <span style={{ marginTop:15, fontSize:19, fontWeight:760, color:'#EDEBEF', lineHeight:1.25 }}>Scientific computing & 3D visualization</span>
      <span style={{ marginTop:10, fontSize:11.5, color:'#968FA3', lineHeight:1.5 }}>Building visual and computational tools for understanding complex subsurface data.</span>
    </div>
  </div>
</div>
```

```aura width=800 height=295
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 28px', background:'#100C17', border:'1px solid #2B2537', borderRadius:20, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:14 }}>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
    <span style={{ fontSize:23, fontWeight:800, color:'#EDEBEF' }}>Leadership</span>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
  </div>
  <div style={{ width:70, height:1, margin:'9px auto 0', background:'#EEB32B', opacity:.7 }}></div>

  <div style={{ display:'flex', gap:13, flex:1, marginTop:21 }}>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', width:440, padding:'21px 23px', background:'#171320', border:'1px solid rgba(238,179,43,.28)', borderRadius:16 }}>
      <span style={{ fontSize:9, fontWeight:800, color:'#EEB32B', letterSpacing:1.7 }}>MUSLIM TECH COLLABORATIVE · UC BERKELEY</span>
      <span style={{ marginTop:9, fontSize:26, fontWeight:800, color:'#EDEBEF' }}>President</span>
      <span style={{ marginTop:10, fontSize:11.5, color:'#968FA3', lineHeight:1.55 }}>Building a stronger Muslim tech community through career access, mentorship, events, and shared opportunity.</span>
    </div>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'21px', background:'#171320', border:'1px solid #2B2537', borderRadius:16 }}>
      <span style={{ fontSize:9, color:'#968FA3', letterSpacing:1.6 }}>TECH HOT TAKE</span>
      <span style={{ marginTop:10, fontSize:20, fontWeight:780, color:'#EEB32B', lineHeight:1.3 }}>Gatekeeping makes tech worse.</span>
      <span style={{ marginTop:9, fontSize:11.5, color:'#968FA3', lineHeight:1.5 }}>Share the playbook. Open the door. Leave the ladder down.</span>
    </div>
  </div>
</div>
```

```aura width=800 height=290
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 28px', background:'#171320', border:'1px solid #2B2537', borderRadius:20, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:14 }}>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
    <span style={{ fontSize:23, fontWeight:800, color:'#EDEBEF' }}>Toolkit</span>
    <svg width="78" height="20"><path d="M0 10 Q10 0 20 10 T40 10 T60 10 T80 10" fill="none" stroke="#EEB32B" opacity=".3"/></svg>
  </div>
  <div style={{ width:70, height:1, margin:'9px auto 0', background:'#EEB32B', opacity:.7 }}></div>

  <div style={{ display:'flex', flexDirection:'column', gap:11, marginTop:21 }}>
    {[
      ['LANGUAGES',['Python','C++','Java','JavaScript','Swift']],
      ['ENGINEERING',['React','Next.js','Node.js','Django','GraphQL','Firebase']],
      ['AI + DATA',['PyTorch','NumPy','Pandas','Matplotlib','Scientific Computing']],
      ['WORKFLOW',['Git','GitHub','Linux','Figma','Notion','LaTeX']]
    ].map((row) => (
      <div key={row[0]} style={{ display:'flex', alignItems:'center' }}>
        <span style={{ width:100, flexShrink:0, fontSize:8.5, fontWeight:700, color:'#968FA3', letterSpacing:1.5 }}>{row[0]}</span>
        <div style={{ display:'flex', gap:7, flexWrap:'wrap' }}>
          {row[1].map((tool) => (
            <span key={tool} style={{ padding:'6px 10px', borderRadius:7, background:'#100C17', border:'1px solid #2B2537', color:'rgba(237,235,239,.78)', fontSize:10.5, fontWeight:600 }}>{tool}</span>
          ))}
        </div>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=245
<div style={{ position:'relative', display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'25px 28px', background:'#100C17', border:'1px solid #2B2537', borderRadius:20, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <svg width="800" height="245" style={{ position:'absolute', top:0, left:0 }}>
    <defs><radialGradient id="ghGlow" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(238,179,43,.11)"/><stop offset="100%" stopColor="rgba(238,179,43,0)"/></radialGradient></defs>
    <ellipse cx="700" cy="230" rx="250" ry="170" fill="url(#ghGlow)" />
  </svg>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
    <div style={{ display:'flex', flexDirection:'column' }}>
      <span style={{ fontSize:9, fontWeight:800, color:'#EEB32B', letterSpacing:1.9 }}>GITHUB</span>
      <span style={{ marginTop:4, fontSize:22, fontWeight:800, color:'#EDEBEF' }}>Live engineering pulse</span>
    </div>
    <span style={{ fontSize:10, color:'#968FA3' }}>@{(github && github.user && github.user.login) || 'hebaalazzeh'}</span>
  </div>

  <div style={{ display:'flex', gap:10, marginTop:20 }}>
    {[
      ['REPOSITORIES', github && github.stats ? github.stats.totalRepos : '—'],
      ['COMMITS', github && github.stats ? github.stats.totalCommits : '—'],
      ['STARS', github && github.stats ? github.stats.totalStars : '—'],
      ['FOLLOWERS', github && github.user ? github.user.followers : '—']
    ].map((stat, i) => (
      <div key={stat[0]} style={{ display:'flex', flexDirection:'column', flex:1, padding:'15px 16px', background:i===2 ? 'rgba(238,179,43,.075)' : '#171320', border:i===2 ? '1px solid rgba(238,179,43,.32)' : '1px solid #2B2537', borderRadius:13 }}>
        <span style={{ fontSize:8, color:'#968FA3', letterSpacing:1.3 }}>{stat[0]}</span>
        <span style={{ marginTop:6, fontSize:25, fontWeight:800, color:i===2 ? '#EEB32B' : '#EDEBEF' }}>{stat[1]}</span>
      </div>
    ))}
  </div>
  <span style={{ marginTop:11, fontSize:9, color:'rgba(150,143,163,.55)' }}>auto-generated by readme-aura · live values update in GitHub Actions</span>
</div>
```

```aura width=800 height=210
<div style={{ position:'relative', display:'flex', flexDirection:'column', alignItems:'center', justifyContent:'center', width:'100%', height:'100%', background:'#171320', border:'1px solid #2B2537', borderRadius:20, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <style>{`
    @keyframes endPulse { 0%,100% { opacity:.16 } 50% { opacity:.50 } }
    #end-ring { animation:endPulse 4.5s ease-in-out infinite; }
  `}</style>
  <svg width="800" height="210" style={{ position:'absolute', top:0, left:0 }}>
    <defs><radialGradient id="endGlow" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(238,179,43,.13)"/><stop offset="100%" stopColor="rgba(238,179,43,0)"/></radialGradient></defs>
    <ellipse cx="400" cy="105" rx="300" ry="150" fill="url(#endGlow)" />
    <circle id="end-ring" cx="400" cy="105" r="64" fill="none" stroke="#EEB32B" opacity=".25" />
  </svg>
  <span style={{ fontSize:9, fontWeight:800, color:'#EEB32B', letterSpacing:2.5, textTransform:'uppercase' }}>the operating principle</span>
  <span style={{ marginTop:13, fontSize:28, fontWeight:800, color:'#EDEBEF', letterSpacing:-.7, textAlign:'center' }}>build boldly. share generously.<br/>leave the ladder down.</span>
  <span style={{ marginTop:12, fontSize:10.5, color:'#968FA3' }}>software engineer · researcher · community builder</span>
</div>
```

```aura width=170 height=46 link="https://github.com/hebaalazzeh" inline align=center
<div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:8, width:'100%', height:'100%', background:'#171320', border:'1px solid #2B2537', borderRadius:10, fontFamily:'Inter, sans-serif' }}>
  <span style={{ color:'#EEB32B', fontSize:15 }}>↗</span><span style={{ color:'#EDEBEF', fontSize:12, fontWeight:700 }}>GitHub</span>
</div>
```
```aura width=170 height=46 link="https://www.linkedin.com/in/heba-alazzeh/" inline align=center
<div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:8, width:'100%', height:'100%', background:'#171320', border:'1px solid #2B2537', borderRadius:10, fontFamily:'Inter, sans-serif' }}>
  <span style={{ color:'#EEB32B', fontSize:15 }}>↗</span><span style={{ color:'#EDEBEF', fontSize:12, fontWeight:700 }}>LinkedIn</span>
</div>
```
```aura width=170 height=46 link="https://hebaalazzeh.github.io/" inline align=center
<div style={{ display:'flex', alignItems:'center', justifyContent:'center', gap:8, width:'100%', height:'100%', background:'#171320', border:'1px solid #2B2537', borderRadius:10, fontFamily:'Inter, sans-serif' }}>
  <span style={{ color:'#EEB32B', fontSize:15 }}>↗</span><span style={{ color:'#EDEBEF', fontSize:12, fontWeight:700 }}>Portfolio</span>
</div>
```

<p align="center"><sub>designed to mirror <a href="https://hebaalazzeh.github.io/">hebaalazzeh.github.io</a> · rendered with <a href="https://github.com/collectioneur/readme-aura">readme-aura</a></sub></p>
