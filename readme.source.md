

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- HERO SECTION — Animated banner with name, subtitle, floating orbs -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=320
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.08)'
}}>

  <style>{`
    @keyframes hero-orb-a { 0%, 100% { transform: translate(0,0); opacity: 0.55; } 50% { transform: translate(40px,-30px); opacity: 0.85; } }
    @keyframes hero-orb-b { 0%, 100% { transform: translate(0,0); opacity: 0.45; } 50% { transform: translate(-35px,25px); opacity: 0.75; } }
    @keyframes hero-orb-c { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-40px); opacity: 0.65; } }
    @keyframes hero-orb-d { 0%, 100% { transform: translate(0,0); opacity: 0.40; } 50% { transform: translate(-20px,-15px); opacity: 0.70; } }
    @keyframes hero-ring { 0%, 100% { opacity: 0.04; } 50% { opacity: 0.14; } }
    @keyframes hero-ring-b { 0%, 100% { opacity: 0.03; } 50% { opacity: 0.10; } }
    @keyframes hero-dot-spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    @keyframes hero-line-scan { 0% { transform: translateY(-320px); } 100% { transform: translateY(320px); } }
    @keyframes hero-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    #ho1 { animation: hero-orb-a 9s ease-in-out infinite; }
    #ho2 { animation: hero-orb-b 12s ease-in-out infinite 0.6s; }
    #ho3 { animation: hero-orb-c 8s ease-in-out infinite 1.5s; }
    #ho4 { animation: hero-orb-d 11s ease-in-out infinite 0.3s; }
    #ho5 { animation: hero-orb-a 10s ease-in-out infinite 2s; }
    #ho6 { animation: hero-orb-b 14s ease-in-out infinite 1s; }
    #hr1 { animation: hero-ring 9s ease-in-out infinite; }
    #hr2 { animation: hero-ring 9s ease-in-out infinite 1.5s; }
    #hr3 { animation: hero-ring-b 9s ease-in-out infinite 3s; }
    #hr4 { animation: hero-ring-b 10s ease-in-out infinite 4.5s; }
    #hdot { animation: hero-dot-spin 24s linear infinite; }
    #hscan { animation: hero-line-scan 6s linear infinite; }
    #hcur { animation: hero-cursor 1.1s step-end infinite; }
  `}</style>

  <svg width="860" height="320" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.50)" />
        <stop offset="60%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.55)" />
        <stop offset="55%" stopColor="rgba(139,92,246,0.15)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.45)" />
        <stop offset="60%" stopColor="rgba(51,102,255,0.10)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.30)" />
        <stop offset="70%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,180,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,180,255,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168,85,247,0.40)" />
        <stop offset="100%" stopColor="rgba(168,85,247,0)" />
      </radialGradient>
      <linearGradient id="hscan-g" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(0,229,255,0)" />
        <stop offset="45%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="50%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="55%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </linearGradient>
    </defs>

    <ellipse id="ho1" cx="120" cy="280" rx="280" ry="200" fill="url(#hg1)" />
    <ellipse id="ho2" cx="740" cy="60"  rx="250" ry="190" fill="url(#hg2)" />
    <ellipse id="ho3" cx="430" cy="310" rx="200" ry="160" fill="url(#hg3)" />
    <ellipse id="ho4" cx="680" cy="290" rx="180" ry="140" fill="url(#hg4)" />
    <ellipse id="ho5" cx="250" cy="40"  rx="220" ry="160" fill="url(#hg5)" />
    <ellipse id="ho6" cx="500" cy="60"  rx="160" ry="130" fill="url(#hg6)" />

    <circle id="hr1" cx="430" cy="160" r="55"  fill="none" stroke="rgba(0,229,255,0.7)" strokeWidth="0.5" />
    <circle id="hr2" cx="430" cy="160" r="100" fill="none" stroke="rgba(139,92,246,0.6)" strokeWidth="0.5" />
    <circle id="hr3" cx="430" cy="160" r="155" fill="none" stroke="rgba(51,102,255,0.5)" strokeWidth="0.4" />
    <circle id="hr4" cx="430" cy="160" r="220" fill="none" stroke="rgba(0,229,255,0.3)" strokeWidth="0.3" />

    <g id="hdot">
      <circle cx="430" cy="105" r="2" fill="rgba(0,229,255,0.6)" />
    </g>

    <rect id="hscan" x="0" y="0" width="860" height="320" fill="url(#hscan-g)" />
  </svg>

  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{
      fontSize: 11, letterSpacing: 6, textTransform: 'uppercase',
      color: 'rgba(0,229,255,0.50)', fontWeight: 300, marginBottom: 14
    }}>full stack engineer</span>

    <span style={{
      fontSize: 56, fontWeight: 800, letterSpacing: -2, lineHeight: 1,
      color: '#ffffff',
      textShadow: '0 0 60px rgba(0,229,255,0.25), 0 0 120px rgba(139,92,246,0.15)'
    }}>Alan Thomas</span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 16, gap: 6 }}>
      <span style={{
        fontSize: 15, color: 'rgba(180,190,255,0.70)', fontWeight: 400,
        letterSpacing: 0.5, fontFamily: 'monospace'
      }}>{'>'} Crafting futuristic interfaces & AI-powered systems</span>
      <span id="hcur" style={{ fontSize: 15, color: 'rgba(0,229,255,0.7)', fontFamily: 'monospace' }}>_</span>
    </div>

    <div style={{ display: 'flex', gap: 8, marginTop: 24, flexWrap: 'wrap', justifyContent: 'center' }}>
      {['Frontend Architecture', 'AI Tooling', 'System Design', 'Developer Experience'].map(function(tag, i) {
        return (
          <span key={i} style={{
            padding: '5px 14px', borderRadius: 100,
            background: 'rgba(0,229,255,0.04)',
            border: '1px solid rgba(0,229,255,0.12)',
            color: 'rgba(0,229,255,0.65)', fontSize: 11, fontWeight: 500, letterSpacing: 0.8
          }}>{tag}</span>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- TECH STACK SECTION — Animated glowing technology cards         -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=260
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes ts-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(30px,-20px); opacity: 0.7; } }
    @keyframes ts-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(-25px,15px); opacity: 0.6; } }
    @keyframes ts-pulse { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
    #tso1 { animation: ts-orb1 10s ease-in-out infinite; }
    #tso2 { animation: ts-orb2 13s ease-in-out infinite 1s; }
    #tso3 { animation: ts-orb1 9s ease-in-out infinite 2s; }
    #tsp1 { animation: ts-pulse 3s ease-in-out infinite; }
    #tsp2 { animation: ts-pulse 3s ease-in-out infinite 0.5s; }
    #tsp3 { animation: ts-pulse 3s ease-in-out infinite 1s; }
    #tsp4 { animation: ts-pulse 3s ease-in-out infinite 1.5s; }
    #tsp5 { animation: ts-pulse 3s ease-in-out infinite 2s; }
    #tsp6 { animation: ts-pulse 3s ease-in-out infinite 0.3s; }
    #tsp7 { animation: ts-pulse 3s ease-in-out infinite 0.8s; }
    #tsp8 { animation: ts-pulse 3s ease-in-out infinite 1.3s; }
    #tsp9 { animation: ts-pulse 3s ease-in-out infinite 1.8s; }
  `}</style>

  <svg width="860" height="260" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="tsg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.35)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="tsg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.30)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="tsg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.30)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="tso1" cx="150" cy="220" rx="200" ry="160" fill="url(#tsg1)" />
    <ellipse id="tso2" cx="700" cy="50"  rx="180" ry="140" fill="url(#tsg2)" />
    <ellipse id="tso3" cx="430" cy="240" rx="160" ry="120" fill="url(#tsg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>tech stack</span>

  <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12, justifyContent: 'center', zIndex: 10, maxWidth: 760, padding: '0 20px' }}>
    {[
      { name: 'React', color: '97,218,251' },
      { name: 'TypeScript', color: '0,122,204' },
      { name: 'Next.js', color: '255,255,255' },
      { name: 'Node.js', color: '104,159,56' },
      { name: 'NestJS', color: '234,63,80' },
      { name: 'Python', color: '55,118,171' },
      { name: 'PostgreSQL', color: '51,103,145' },
      { name: 'Docker', color: '13,183,237' },
      { name: 'GitHub Actions', color: '33,136,255' },
    ].map(function(tech, i) {
      return (
        <div key={i} id={'tsp' + (i + 1)} style={{
          display: 'flex', alignItems: 'center', gap: 8,
          padding: '10px 20px', borderRadius: 12,
          background: 'rgba(' + tech.color + ',0.06)',
          border: '1px solid rgba(' + tech.color + ',0.18)',
        }}>
          <div style={{
            width: 8, height: 8, borderRadius: 4,
            background: 'rgba(' + tech.color + ',0.8)',
            boxShadow: '0 0 8px rgba(' + tech.color + ',0.5)'
          }} />
          <span style={{
            fontSize: 13, fontWeight: 500,
            color: 'rgba(255,255,255,0.75)', letterSpacing: 0.3
          }}>{tech.name}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- ABOUT ME SECTION — Terminal-style glassmorphism panel          -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=240
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(51,102,255,0.08)'
}}>

  <style>{`
    @keyframes ab-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.5; } 50% { transform: translate(25px,-18px); opacity: 0.8; } }
    @keyframes ab-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(-20px,14px); opacity: 0.65; } }
    @keyframes ab-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    @keyframes ab-line-glow { 0%, 100% { opacity: 0.15; } 50% { opacity: 0.35; } }
    #abo1 { animation: ab-orb1 9s ease-in-out infinite; }
    #abo2 { animation: ab-orb2 11s ease-in-out infinite 1.5s; }
    #abcur { animation: ab-cursor 1.1s step-end infinite; }
    #abline { animation: ab-line-glow 4s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="240" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="abg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="abg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
    </defs>
    <ellipse id="abo1" cx="80"  cy="200" rx="200" ry="150" fill="url(#abg1)" />
    <ellipse id="abo2" cx="780" cy="60"  rx="180" ry="140" fill="url(#abg2)" />
    <line id="abline" x1="44" y1="70" x2="44" y2="200" stroke="rgba(0,229,255,0.25)" strokeWidth="1" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    justifyContent: 'center', padding: '0 56px', zIndex: 10, gap: 10, flex: 1
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(51,102,255,0.50)', fontWeight: 300, marginBottom: 6
    }}>about</span>

    <span style={{ fontSize: 22, fontWeight: 700, color: '#ffffff', lineHeight: 1.3 }}>
      Frontend-focused full stack engineer
    </span>

    <span style={{
      fontSize: 14, color: 'rgba(255,255,255,0.50)', lineHeight: 1.7,
      maxWidth: 620
    }}>
      I build high-performance interfaces, design scalable frontend systems, and craft developer tools. My work sits at the intersection of engineering precision and visual excellence — from complex React architectures to AI-powered agent systems and real-time data platforms.
    </span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 8 }}>
      <span style={{ fontSize: 13, color: 'rgba(0,229,255,0.45)', fontFamily: 'monospace' }}>
        {'>'} passionate about UI systems · scalable architecture · developer experience
      </span>
      <span id="abcur" style={{ fontSize: 13, color: 'rgba(0,229,255,0.6)', fontFamily: 'monospace', marginLeft: 1 }}>_</span>
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FEATURED PROJECTS — Rich project cards with animated glow borders -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=490
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.06)', padding: '28px 0'
}}>

  <style>{`
    @keyframes pj-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(35px,-25px); opacity: 0.55; } }
    @keyframes pj-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.25; } 50% { transform: translate(-30px,20px); opacity: 0.5; } }
    @keyframes pj-orb3 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(20px,15px); opacity: 0.5; } }
    @keyframes pj-status { 0%, 100% { opacity: 0.5; } 50% { opacity: 1; } }
    #pjo1 { animation: pj-orb1 10s ease-in-out infinite; }
    #pjo2 { animation: pj-orb2 13s ease-in-out infinite 1s; }
    #pjo3 { animation: pj-orb3 11s ease-in-out infinite 2s; }
    #pjs1 { animation: pj-status 2s ease-in-out infinite; }
    #pjs2 { animation: pj-status 2s ease-in-out infinite 0.4s; }
    #pjs3 { animation: pj-status 2s ease-in-out infinite 0.8s; }
    #pjs4 { animation: pj-status 2s ease-in-out infinite 1.2s; }
    #pjs5 { animation: pj-status 2s ease-in-out infinite 1.6s; }
  `}</style>

  <svg width="860" height="490" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="pjg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.20)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="pjg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.22)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="pjg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.18)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
    </defs>
    <ellipse id="pjo1" cx="100" cy="400" rx="220" ry="180" fill="url(#pjg1)" />
    <ellipse id="pjo2" cx="760" cy="100" rx="200" ry="160" fill="url(#pjg2)" />
    <ellipse id="pjo3" cx="430" cy="450" rx="180" ry="140" fill="url(#pjg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(0,229,255,0.45)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>featured projects</span>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 10, zIndex: 10, width: '100%', padding: '0 28px' }}>
    {[
      {
        title: 'Procurement Management Platform',
        desc: 'End-to-end procurement system with advanced data flows, role-based access, and real-time dashboards',
        tech: 'React · TypeScript · NestJS · PostgreSQL',
        color: '0,229,255',
        statusId: 'pjs1'
      },
      {
        title: 'Authentication Platform',
        desc: 'Secure, scalable auth system with OAuth2, MFA support, and session management infrastructure',
        tech: 'Next.js · Node.js · PostgreSQL · JWT',
        color: '139,92,246',
        statusId: 'pjs2'
      },
      {
        title: 'Futuristic React Flow UI System',
        desc: 'Node-based visual editor with futuristic aesthetics, custom nodes, and real-time collaboration',
        tech: 'React Flow · TypeScript · Canvas · WebSocket',
        color: '51,102,255',
        statusId: 'pjs3'
      },
      {
        title: 'AI Agent Tooling Platform',
        desc: 'Experimental AI agent orchestration with RAG pipelines, tool calling, and structured reasoning',
        tech: 'Python · LangChain · React · FastAPI',
        color: '236,72,153',
        statusId: 'pjs4'
      },
      {
        title: 'Trading Simulator Engine',
        desc: 'Real-time market simulation with charting, order management, and portfolio analytics interface',
        tech: 'React · TypeScript · Node.js · WebSocket',
        color: '168,85,247',
        statusId: 'pjs5'
      }
    ].map(function(project, i) {
      return (
        <div key={i} style={{
          display: 'flex', alignItems: 'center', padding: '14px 20px',
          background: 'rgba(255,255,255,0.02)',
          border: '1px solid rgba(' + project.color + ',0.12)',
          borderRadius: 12, gap: 14
        }}>
          <div id={project.statusId} style={{
            width: 8, height: 8, borderRadius: 4, flexShrink: 0,
            background: 'rgba(' + project.color + ',0.8)',
            boxShadow: '0 0 10px rgba(' + project.color + ',0.4)'
          }} />
          <div style={{ display: 'flex', flexDirection: 'column', gap: 3, flex: 1 }}>
            <span style={{ fontSize: 14, fontWeight: 600, color: '#ffffff', letterSpacing: 0.2 }}>
              {project.title}
            </span>
            <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.40)', lineHeight: 1.4 }}>
              {project.desc}
            </span>
          </div>
          <span style={{
            fontSize: 10, color: 'rgba(' + project.color + ',0.55)',
            fontFamily: 'monospace', letterSpacing: 0.3, textAlign: 'right',
            flexShrink: 0, maxWidth: 200
          }}>{project.tech}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- GITHUB STATS — Cohesive themed statistics                      -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<p align="center">

![](https://github-readme-stats.vercel.app/api?username=alan-thomas-shaji&show_icons=true&theme=transparent&hide_border=true&title_color=00e5ff&text_color=8b9dc3&icon_color=8b5cf6&bg_color=00000000&ring_color=00e5ff)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=alan-thomas-shaji&layout=compact&theme=transparent&hide_border=true&title_color=00e5ff&text_color=8b9dc3&bg_color=00000000)

</p>

<p align="center">

![](https://github-readme-streak-stats.herokuapp.com/?user=alan-thomas-shaji&theme=transparent&hide_border=true&ring=00e5ff&fire=8b5cf6&currStreakLabel=00e5ff&sideLabels=8b9dc3&currStreakNum=ffffff&sideNums=ffffff&dates=555555&stroke=1a1a2e)

</p>

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CURRENT FOCUS — What I'm building and exploring                -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=220
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes cf-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-18px); opacity: 0.6; } }
    @keyframes cf-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(-20px,14px); opacity: 0.55; } }
    @keyframes cf-dot { 0%, 100% { opacity: 0.4; } 50% { opacity: 1; } }
    #cfo1 { animation: cf-orb1 10s ease-in-out infinite; }
    #cfo2 { animation: cf-orb2 12s ease-in-out infinite 1s; }
    #cfd1 { animation: cf-dot 2.5s ease-in-out infinite; }
    #cfd2 { animation: cf-dot 2.5s ease-in-out infinite 0.4s; }
    #cfd3 { animation: cf-dot 2.5s ease-in-out infinite 0.8s; }
    #cfd4 { animation: cf-dot 2.5s ease-in-out infinite 1.2s; }
    #cfd5 { animation: cf-dot 2.5s ease-in-out infinite 1.6s; }
    #cfd6 { animation: cf-dot 2.5s ease-in-out infinite 2.0s; }
  `}</style>

  <svg width="860" height="220" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="cfg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="cfg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.25)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="cfo1" cx="120" cy="190" rx="200" ry="150" fill="url(#cfg1)" />
    <ellipse id="cfo2" cx="740" cy="50"  rx="180" ry="140" fill="url(#cfg2)" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    padding: '24px 40px', zIndex: 10, flex: 1, justifyContent: 'center'
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 16
    }}>currently exploring</span>

    <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
      {[
        { label: 'AI Agents & RAG Systems', color: '0,229,255', id: 'cfd1' },
        { label: 'Scalable Frontend Architecture', color: '139,92,246', id: 'cfd2' },
        { label: 'Distributed Systems', color: '51,102,255', id: 'cfd3' },
        { label: 'Advanced UI Engineering', color: '236,72,153', id: 'cfd4' },
        { label: 'Realtime Data Platforms', color: '168,85,247', id: 'cfd5' },
        { label: 'LLM Orchestration', color: '0,180,255', id: 'cfd6' },
      ].map(function(item, i) {
        return (
          <div key={i} style={{
            display: 'flex', alignItems: 'center', gap: 8,
            padding: '8px 16px', borderRadius: 10,
            background: 'rgba(' + item.color + ',0.04)',
            border: '1px solid rgba(' + item.color + ',0.12)'
          }}>
            <div id={item.id} style={{
              width: 6, height: 6, borderRadius: 3,
              background: 'rgba(' + item.color + ',0.9)',
              boxShadow: '0 0 8px rgba(' + item.color + ',0.5)'
            }} />
            <span style={{
              fontSize: 12, color: 'rgba(255,255,255,0.60)',
              fontWeight: 500, letterSpacing: 0.3
            }}>{item.label}</span>
          </div>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- SOCIAL LINKS — Custom SocialMediaButton components             -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=130 height=44 link="https://github.com/alan-thomas-shaji" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/github/ffffff"
  text="GitHub"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#00e5ff' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#8b5cf6' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#00e5ff' },
  ]}
  iconSize="18"
/>
```

```aura width=140 height=44 link="https://www.linkedin.com/in/alan-thomas-shaji/" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/linkedin/0A66C2"
  text="LinkedIn"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={140}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#0A66C2' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#00e5ff' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#0A66C2' },
  ]}
  iconSize="18"
/>
```

```aura width=140 height=44 link="#" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/googlechrome/ffffff"
  text="Portfolio"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={140}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#8b5cf6' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#ec4899' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#8b5cf6' },
  ]}
  iconSize="18"
/>
```

```aura width=120 height=44 link="mailto:alanthomas@email.com" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/gmail/EA4335"
  text="Email"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#EA4335' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#ec4899' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#EA4335' },
  ]}
  iconSize="18"
/>
```

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FOOTER — Animated scanline + terminal aesthetic                    -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=80
<div style={{
  width: '100%', height: '100%', background: '#06060a',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(0,229,255,0.05)'
}}>

  <style>{`
    @keyframes ft-scan { 0% { transform: translateY(-80px); } 100% { transform: translateY(80px); } }
    @keyframes ft-pulse { 0%, 100% { opacity: 0.3; } 50% { opacity: 0.7; } }
    @keyframes ft-orb { 0%, 100% { transform: translate(0,0); opacity: 0.25; } 50% { transform: translate(30px,-10px); opacity: 0.45; } }
    #ftscan { animation: ft-scan 4s linear infinite; }
    #ftd1 { animation: ft-pulse 3s ease-in-out infinite; }
    #ftd2 { animation: ft-pulse 3s ease-in-out infinite 1s; }
    #ftd3 { animation: ft-pulse 3s ease-in-out infinite 2s; }
    #ftorb1 { animation: ft-orb 8s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="80" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <linearGradient id="fsg" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(0,229,255,0)" />
        <stop offset="45%" stopColor="rgba(0,229,255,0.03)" />
        <stop offset="50%" stopColor="rgba(0,229,255,0.08)" />
        <stop offset="55%" stopColor="rgba(0,229,255,0.03)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </linearGradient>
      <radialGradient id="ftg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.25)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
    </defs>

    <line x1="0" y1="1" x2="860" y2="1" stroke="rgba(0,229,255,0.06)" strokeWidth="1" />

    <ellipse id="ftorb1" cx="430" cy="40" rx="300" ry="60" fill="url(#ftg1)" />
    <rect id="ftscan" x="0" y="0" width="860" height="80" fill="url(#fsg)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 6, zIndex: 10 }}>
    <div id="ftd1" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(0,229,255,0.6)' }} />
    <div id="ftd2" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(139,92,246,0.6)' }} />
    <div id="ftd3" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(236,72,153,0.6)' }} />
  </div>

  <span style={{
    fontSize: 11, color: 'rgba(255,255,255,0.20)', letterSpacing: 3,
    fontWeight: 300, marginTop: 8, zIndex: 10
  }}>crafted with precision · powered by readme-aura</span>
</div>
```
