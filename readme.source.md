```aura width=800 height=420
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'space-between', width: '100%', height: '100%', padding: '34px 38px', background: '#05070D', borderRadius: 28, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(255,255,255,0.08)' }}>
  <style>{`
    @keyframes driftA { 0%,100% { transform: translate(0,0); opacity:.65 } 50% { transform: translate(26px,-18px); opacity:1 } }
    @keyframes driftB { 0%,100% { transform: translate(0,0); opacity:.45 } 50% { transform: translate(-22px,22px); opacity:.8 } }
    @keyframes pulseRing { 0%,100% { opacity:.10 } 50% { opacity:.32 } }
    @keyframes spin { from { transform: rotate(0deg) } to { transform: rotate(360deg) } }
    @keyframes blink { 0%,45% { opacity:1 } 46%,100% { opacity:.15 } }
    #hero-blue { animation: driftA 9s ease-in-out infinite; }
    #hero-gold { animation: driftB 11s ease-in-out infinite 1s; }
    #hero-violet { animation: driftA 13s ease-in-out infinite 2s; }
    #hero-ring-1 { animation: pulseRing 5s ease-in-out infinite; }
    #hero-ring-2 { animation: pulseRing 7s ease-in-out infinite 1.2s; }
    #hero-ring-3 { animation: pulseRing 9s ease-in-out infinite 2.4s; }
    #hero-orbit { transform-origin: 620px 156px; animation: spin 22s linear infinite; }
    #hero-live { animation: blink 1.8s ease-in-out infinite; }
  `}</style>

  <svg width="800" height="420" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="heroBlue" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,85,180,.50)" />
        <stop offset="100%" stopColor="rgba(0,85,180,0)" />
      </radialGradient>
      <radialGradient id="heroGold" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(253,181,21,.38)" />
        <stop offset="100%" stopColor="rgba(253,181,21,0)" />
      </radialGradient>
      <radialGradient id="heroViolet" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(167,139,250,.30)" />
        <stop offset="100%" stopColor="rgba(167,139,250,0)" />
      </radialGradient>
      <linearGradient id="heroLine" x1="0" x2="1">
        <stop offset="0%" stopColor="rgba(0,85,180,0)" />
        <stop offset="45%" stopColor="rgba(93,173,255,.65)" />
        <stop offset="70%" stopColor="rgba(253,181,21,.75)" />
        <stop offset="100%" stopColor="rgba(253,181,21,0)" />
      </linearGradient>
    </defs>
    <ellipse id="hero-blue" cx="90" cy="330" rx="330" ry="260" fill="url(#heroBlue)" />
    <ellipse id="hero-gold" cx="720" cy="80" rx="250" ry="220" fill="url(#heroGold)" />
    <ellipse id="hero-violet" cx="590" cy="390" rx="250" ry="180" fill="url(#heroViolet)" />
    <circle id="hero-ring-1" cx="620" cy="156" r="52" fill="none" stroke="rgba(255,255,255,.7)" strokeWidth=".7" />
    <circle id="hero-ring-2" cx="620" cy="156" r="88" fill="none" stroke="rgba(255,255,255,.6)" strokeWidth=".7" />
    <circle id="hero-ring-3" cx="620" cy="156" r="130" fill="none" stroke="rgba(255,255,255,.45)" strokeWidth=".7" />
    <g id="hero-orbit">
      <circle cx="620" cy="68" r="4" fill="#FDB515" />
      <circle cx="620" cy="68" r="9" fill="none" stroke="rgba(253,181,21,.35)" />
    </g>
    <path d="M40 318 H760" stroke="url(#heroLine)" strokeWidth="1" />
  </svg>

  <div style={{ position:'relative', display:'flex', alignItems:'center', justifyContent:'space-between', zIndex:5 }}>
    <div style={{ display:'flex', alignItems:'center', gap:8, padding:'7px 12px', border:'1px solid rgba(255,255,255,.10)', borderRadius:999, background:'rgba(255,255,255,.035)' }}>
      <span id="hero-live" style={{ width:7, height:7, borderRadius:999, background:'#FDB515' }}></span>
      <span style={{ fontSize:10, fontWeight:700, color:'rgba(255,255,255,.70)', letterSpacing:2.1, textTransform:'uppercase' }}>building in public</span>
    </div>
    <span style={{ fontSize:10, color:'rgba(255,255,255,.28)', letterSpacing:2.2, textTransform:'uppercase' }}>berkeley · bay area</span>
  </div>

  <div style={{ position:'relative', display:'flex', flexDirection:'column', zIndex:5, marginTop:18 }}>
    <span style={{ fontSize:14, fontWeight:600, color:'#FDB515', letterSpacing:3.2, textTransform:'uppercase', marginBottom:10 }}>software engineer · ai researcher · community builder</span>
    <span style={{ fontSize:66, fontWeight:800, color:'#FFFFFF', letterSpacing:-3.2, lineHeight:.98 }}>Heba Alazzeh</span>
    <span style={{ maxWidth:590, marginTop:18, fontSize:18, color:'rgba(255,255,255,.62)', lineHeight:1.45, letterSpacing:-.15 }}>I build technology that moves from research → real people → real impact.</span>
  </div>

  <div style={{ position:'relative', display:'flex', alignItems:'center', gap:10, zIndex:5 }}>
    {['UC BERKELEY CS','GOOGLE SWE','STANFORD AI RESEARCH'].map((item, i) => (
      <span key={item} style={{ padding:'8px 13px', borderRadius:999, fontSize:10, fontWeight:700, letterSpacing:1.4, color: i === 1 ? '#06111E' : 'rgba(255,255,255,.72)', background: i === 1 ? '#FDB515' : 'rgba(255,255,255,.045)', border: i === 1 ? '1px solid #FDB515' : '1px solid rgba(255,255,255,.10)' }}>{item}</span>
    ))}
  </div>
</div>
```

```aura width=800 height=280
<div style={{ display:'flex', gap:14, width:'100%', height:'100%', fontFamily:'Inter, sans-serif' }}>
  <div style={{ position:'relative', display:'flex', flexDirection:'column', justifyContent:'space-between', width:510, height:'100%', padding:'26px 28px', background:'#080B13', border:'1px solid rgba(255,255,255,.08)', borderRadius:22, overflow:'hidden' }}>
    <svg width="510" height="280" style={{ position:'absolute', top:0, left:0 }}>
      <defs>
        <radialGradient id="aboutGlow" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(0,85,180,.32)"/><stop offset="100%" stopColor="rgba(0,85,180,0)"/></radialGradient>
      </defs>
      <ellipse cx="40" cy="250" rx="240" ry="170" fill="url(#aboutGlow)" />
      <path d="M330 0 L510 0 L510 180" fill="none" stroke="rgba(253,181,21,.18)" strokeWidth="1" />
      <circle cx="458" cy="54" r="28" fill="none" stroke="rgba(253,181,21,.18)" />
      <circle cx="458" cy="54" r="45" fill="none" stroke="rgba(255,255,255,.05)" />
    </svg>
    <div style={{ position:'relative', display:'flex', flexDirection:'column', zIndex:2 }}>
      <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:2.6, textTransform:'uppercase' }}>01 · about</span>
      <span style={{ marginTop:15, fontSize:30, fontWeight:750, color:'#fff', letterSpacing:-1.2, lineHeight:1.15 }}>Building useful things.<br/>Sharing what I learn.</span>
      <span style={{ marginTop:17, fontSize:14, color:'rgba(255,255,255,.56)', lineHeight:1.55 }}>Computer Science at UC Berkeley, software engineering at Google, and AI research across autonomous systems + scientific computing at Stanford.</span>
    </div>
    <div style={{ position:'relative', display:'flex', alignItems:'center', gap:8, zIndex:2 }}>
      <span style={{ fontFamily:'monospace', fontSize:12, color:'rgba(255,255,255,.44)' }}>{'> '}no gatekeeping. build the ladder, then leave it down.</span>
    </div>
  </div>

  <div style={{ display:'flex', flexDirection:'column', gap:14, flex:1 }}>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'20px 22px', background:'#0A0D15', border:'1px solid rgba(255,255,255,.08)', borderRadius:22 }}>
      <span style={{ fontSize:10, color:'rgba(255,255,255,.34)', letterSpacing:2.2, textTransform:'uppercase' }}>north star</span>
      <span style={{ marginTop:8, fontSize:18, fontWeight:700, color:'#fff', lineHeight:1.25 }}>accessible, ethical technology</span>
    </div>
    <div style={{ display:'flex', flexDirection:'column', justifyContent:'center', flex:1, padding:'20px 22px', background:'#0A0D15', border:'1px solid rgba(255,255,255,.08)', borderRadius:22 }}>
      <span style={{ fontSize:10, color:'rgba(255,255,255,.34)', letterSpacing:2.2, textTransform:'uppercase' }}>currently curious about</span>
      <span style={{ marginTop:8, fontSize:18, fontWeight:700, color:'#FDB515', lineHeight:1.25 }}>AI systems at scale</span>
    </div>
  </div>
</div>
```

```aura width=800 height=310
<div style={{ position:'relative', display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'24px', background:'#05070D', border:'1px solid rgba(255,255,255,.08)', borderRadius:24, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <style>{`
    @keyframes scan { 0% { transform: translateX(-160px); opacity:0 } 20% { opacity:.8 } 80% { opacity:.8 } 100% { transform: translateX(900px); opacity:0 } }
    #orbit-scan { animation: scan 7s linear infinite; }
  `}</style>
  <svg width="800" height="310" style={{ position:'absolute', top:0, left:0 }}>
    <defs><linearGradient id="scanLine" x1="0" x2="1"><stop offset="0%" stopColor="rgba(0,85,180,0)"/><stop offset="50%" stopColor="rgba(253,181,21,.35)"/><stop offset="100%" stopColor="rgba(0,85,180,0)"/></linearGradient></defs>
    <rect id="orbit-scan" x="0" y="0" width="130" height="310" fill="url(#scanLine)" />
    <path d="M0 78 H800 M0 155 H800 M0 232 H800" stroke="rgba(255,255,255,.025)" />
  </svg>
  <div style={{ position:'relative', display:'flex', alignItems:'center', justifyContent:'space-between', zIndex:2, marginBottom:17 }}>
    <div style={{ display:'flex', flexDirection:'column' }}>
      <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:2.6, textTransform:'uppercase' }}>02 · current orbit</span>
      <span style={{ marginTop:5, fontSize:23, fontWeight:750, color:'#fff', letterSpacing:-.7 }}>Where engineering meets impact.</span>
    </div>
    <span style={{ fontFamily:'monospace', fontSize:10, color:'rgba(255,255,255,.28)' }}>STATUS // ACTIVE</span>
  </div>
  <div style={{ position:'relative', display:'flex', gap:12, flex:1, zIndex:2 }}>
    {[
      ['01','Google','Software Engineering','Cloud SDK · performance + architecture','⚡'],
      ['02','Stanford','AI Research','SISL · autonomous systems + Mineral-X','◌'],
      ['03','MTC Berkeley','President','building Muslim tech community @ Cal','✦']
    ].map((x, i) => (
      <div key={x[0]} style={{ display:'flex', flexDirection:'column', justifyContent:'space-between', flex:1, padding:'18px', background: i === 0 ? 'rgba(253,181,21,.055)' : 'rgba(255,255,255,.025)', border: i === 0 ? '1px solid rgba(253,181,21,.25)' : '1px solid rgba(255,255,255,.075)', borderRadius:18 }}>
        <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
          <span style={{ fontFamily:'monospace', fontSize:10, color:'rgba(255,255,255,.30)' }}>{x[0]}</span>
          <span style={{ fontSize:18, color: i === 0 ? '#FDB515' : 'rgba(255,255,255,.65)' }}>{x[4]}</span>
        </div>
        <div style={{ display:'flex', flexDirection:'column' }}>
          <span style={{ fontSize:18, fontWeight:750, color:'#fff' }}>{x[1]}</span>
          <span style={{ marginTop:4, fontSize:12, fontWeight:650, color: i === 0 ? '#FDB515' : '#7DB6FF' }}>{x[2]}</span>
          <span style={{ marginTop:9, fontSize:11, color:'rgba(255,255,255,.42)', lineHeight:1.45 }}>{x[3]}</span>
        </div>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=310
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'24px 26px', background:'#080B13', border:'1px solid rgba(255,255,255,.08)', borderRadius:24, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'flex-end', justifyContent:'space-between' }}>
    <div style={{ display:'flex', flexDirection:'column' }}>
      <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:2.6, textTransform:'uppercase' }}>03 · toolkit</span>
      <span style={{ marginTop:6, fontSize:23, fontWeight:750, color:'#fff', letterSpacing:-.6 }}>My favorite tools for turning ideas into systems.</span>
    </div>
    <span style={{ fontSize:10, color:'rgba(255,255,255,.28)', letterSpacing:1.7 }}>CURATED &gt; EXHAUSTIVE</span>
  </div>
  <div style={{ display:'flex', flexDirection:'column', gap:11, marginTop:22 }}>
    {[
      ['LANGUAGES',['Python','C++','Java','JavaScript','Swift']],
      ['BUILD',['React','Next.js','Node.js','Django','GraphQL','Firebase']],
      ['AI + DATA',['PyTorch','NumPy','Pandas','Matplotlib','Scientific Computing']],
      ['WORKFLOW',['Git','GitHub','Linux','Figma','Notion','LaTeX']]
    ].map((row) => (
      <div key={row[0]} style={{ display:'flex', alignItems:'center' }}>
        <span style={{ width:92, flexShrink:0, fontFamily:'monospace', fontSize:9, color:'rgba(255,255,255,.28)', letterSpacing:1.4 }}>{row[0]}</span>
        <div style={{ display:'flex', gap:7, flexWrap:'wrap' }}>
          {row[1].map((tool) => (
            <span key={tool} style={{ padding:'6px 10px', borderRadius:8, background:'rgba(255,255,255,.035)', border:'1px solid rgba(255,255,255,.075)', color:'rgba(255,255,255,.70)', fontSize:10.5, fontWeight:600 }}>{tool}</span>
          ))}
        </div>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=260
<div style={{ position:'relative', display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'24px 26px', background:'#05070D', border:'1px solid rgba(255,255,255,.08)', borderRadius:24, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <svg width="800" height="260" style={{ position:'absolute', top:0, left:0 }}>
    <defs><radialGradient id="statGlow" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(167,139,250,.20)"/><stop offset="100%" stopColor="rgba(167,139,250,0)"/></radialGradient></defs>
    <ellipse cx="720" cy="250" rx="260" ry="190" fill="url(#statGlow)" />
  </svg>
  <div style={{ position:'relative', display:'flex', alignItems:'center', justifyContent:'space-between', zIndex:2 }}>
    <div style={{ display:'flex', flexDirection:'column' }}>
      <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:2.6, textTransform:'uppercase' }}>04 · github pulse</span>
      <span style={{ marginTop:6, fontSize:23, fontWeight:750, color:'#fff' }}>Live signal from @{(github && github.user && github.user.login) || 'hebaalazzeh'}</span>
    </div>
    <img src={(github && github.user && github.user.avatarUrl) || 'https://github.com/hebaalazzeh.png'} width="46" height="46" style={{ borderRadius:999, border:'1px solid rgba(253,181,21,.55)' }} />
  </div>
  <div style={{ position:'relative', display:'flex', gap:10, marginTop:21, zIndex:2 }}>
    {[
      ['REPOS', github && github.stats ? github.stats.totalRepos : '—'],
      ['COMMITS', github && github.stats ? github.stats.totalCommits : '—'],
      ['STARS', github && github.stats ? github.stats.totalStars : '—'],
      ['FOLLOWERS', github && github.user ? github.user.followers : '—']
    ].map((stat, i) => (
      <div key={stat[0]} style={{ display:'flex', flexDirection:'column', flex:1, padding:'17px 18px', borderRadius:16, background: i === 2 ? 'rgba(253,181,21,.055)' : 'rgba(255,255,255,.025)', border: i === 2 ? '1px solid rgba(253,181,21,.22)' : '1px solid rgba(255,255,255,.075)' }}>
        <span style={{ fontSize:10, color:'rgba(255,255,255,.32)', letterSpacing:1.8 }}>{stat[0]}</span>
        <span style={{ marginTop:7, fontSize:28, fontWeight:800, color: i === 2 ? '#FDB515' : '#fff', letterSpacing:-1 }}>{stat[1]}</span>
      </div>
    ))}
  </div>
  <span style={{ position:'relative', zIndex:2, marginTop:13, fontSize:9.5, color:'rgba(255,255,255,.25)', fontFamily:'monospace' }}>auto-generated by readme-aura · refreshed by GitHub Actions</span>
</div>
```

```aura width=800 height=285
<div style={{ display:'flex', flexDirection:'column', width:'100%', height:'100%', padding:'24px 26px', background:'#080B13', border:'1px solid rgba(255,255,255,.08)', borderRadius:24, fontFamily:'Inter, sans-serif' }}>
  <div style={{ display:'flex', alignItems:'center', justifyContent:'space-between' }}>
    <div style={{ display:'flex', flexDirection:'column' }}>
      <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:2.6, textTransform:'uppercase' }}>05 · impact map</span>
      <span style={{ marginTop:6, fontSize:23, fontWeight:750, color:'#fff' }}>The kind of work I want more of.</span>
    </div>
    <span style={{ fontSize:24, color:'#FDB515' }}>✦</span>
  </div>
  <div style={{ display:'flex', gap:12, flex:1, marginTop:18 }}>
    {[
      ['ENGINEERING','systems that are fast, reliable, and delightful to use','01'],
      ['RESEARCH','AI that can leave the paper and survive the real world','02'],
      ['COMMUNITY','spaces where opportunity is shared instead of gatekept','03']
    ].map((c, i) => (
      <div key={c[0]} style={{ position:'relative', display:'flex', flexDirection:'column', justifyContent:'space-between', flex:1, padding:'18px', borderRadius:18, background: i === 1 ? 'rgba(0,85,180,.07)' : 'rgba(255,255,255,.025)', border: i === 1 ? '1px solid rgba(93,173,255,.22)' : '1px solid rgba(255,255,255,.075)', overflow:'hidden' }}>
        <span style={{ position:'absolute', right:12, top:8, fontSize:48, fontWeight:800, color:'rgba(255,255,255,.025)' }}>{c[2]}</span>
        <span style={{ fontSize:10, fontWeight:750, letterSpacing:1.9, color: i === 1 ? '#7DB6FF' : '#FDB515' }}>{c[0]}</span>
        <span style={{ fontSize:15, fontWeight:650, lineHeight:1.35, color:'rgba(255,255,255,.76)', maxWidth:190 }}>{c[1]}</span>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=220
<div style={{ position:'relative', display:'flex', flexDirection:'column', alignItems:'center', justifyContent:'center', width:'100%', height:'100%', background:'#05070D', border:'1px solid rgba(255,255,255,.08)', borderRadius:24, overflow:'hidden', fontFamily:'Inter, sans-serif' }}>
  <style>{`
    @keyframes footerPulse { 0%,100% { opacity:.12; transform:scale(.94) } 50% { opacity:.38; transform:scale(1.06) } }
    #footer-star { transform-origin:400px 110px; animation:footerPulse 4s ease-in-out infinite; }
  `}</style>
  <svg width="800" height="220" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="footerG" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(253,181,21,.20)"/><stop offset="100%" stopColor="rgba(253,181,21,0)"/></radialGradient>
      <linearGradient id="footerL" x1="0" x2="1"><stop offset="0%" stopColor="rgba(0,85,180,0)"/><stop offset="50%" stopColor="rgba(93,173,255,.50)"/><stop offset="100%" stopColor="rgba(253,181,21,0)"/></linearGradient>
    </defs>
    <ellipse cx="400" cy="110" rx="300" ry="150" fill="url(#footerG)" />
    <circle id="footer-star" cx="400" cy="110" r="58" fill="none" stroke="rgba(253,181,21,.38)" />
    <path d="M110 110 H690" stroke="url(#footerL)" />
  </svg>
  <div style={{ position:'relative', display:'flex', flexDirection:'column', alignItems:'center', zIndex:2 }}>
    <span style={{ fontSize:10, fontWeight:700, color:'#FDB515', letterSpacing:3, textTransform:'uppercase' }}>the operating principle</span>
    <span style={{ marginTop:14, fontSize:29, fontWeight:780, color:'#fff', letterSpacing:-1, textAlign:'center' }}>build boldly. share generously.<br/>leave the ladder down.</span>
    <span style={{ marginTop:14, fontSize:11, color:'rgba(255,255,255,.34)', letterSpacing:1.3 }}>thanks for stopping by · let's build something that matters</span>
  </div>
</div>
```

```aura width=170 height=46 link="https://github.com/hebaalazzeh" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/github/ffffff"
  text="GitHub"
  backgroundColor="#080B13"
  textColor="#F5F7FA"
  borderColor="#2A2F3A"
  width={170}
  height={46}
  iconSize="20"
  gradientStops={[
    { offset: '0%', color: '#0055B4' },
    { offset: '50%', color: '#FDB515' },
    { offset: '100%', color: '#7DB6FF' },
  ]}
/>
```
```aura width=170 height=46 link="https://www.linkedin.com/in/heba-alazzeh/" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/linkedin/ffffff"
  text="LinkedIn"
  backgroundColor="#080B13"
  textColor="#F5F7FA"
  borderColor="#2A2F3A"
  width={170}
  height={46}
  iconSize="20"
  gradientStops={[
    { offset: '0%', color: '#0055B4' },
    { offset: '50%', color: '#7DB6FF' },
    { offset: '100%', color: '#FDB515' },
  ]}
/>
```
```aura width=170 height=46 link="https://hebaalazzeh.github.io/" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/googlechrome/ffffff"
  text="Portfolio"
  backgroundColor="#080B13"
  textColor="#F5F7FA"
  borderColor="#2A2F3A"
  width={170}
  height={46}
  iconSize="20"
  gradientStops={[
    { offset: '0%', color: '#FDB515' },
    { offset: '50%', color: '#A78BFA' },
    { offset: '100%', color: '#0055B4' },
  ]}
/>
```

<p align="center"><sub>crafted with <a href="https://github.com/collectioneur/readme-aura">readme-aura</a> · rendered as GitHub-safe SVG</sub></p>
