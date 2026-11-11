<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#0a0a0a">
<title>Fiel Fitness</title>
<style>
:root {
  color-scheme: dark;
  --bg: #0a0a0a;
  --card: #171717;
  --border: #2d2b31;
  --purple: #a05cf0;
  --purple-light: #bc8af7;
  --text: #f3f0f7;
  --muted: #aaa5b1;
  --danger: #ff7777;
  --success: #81dfa5;
}
* { box-sizing: border-box; }
html { scroll-padding-top: 70px; }
body {
  margin: 0 auto;
  max-width: 640px;
  min-height: 100vh;
  background: var(--bg);
  color: var(--text);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}
button, input, select { font: inherit; }
button { -webkit-tap-highlight-color: transparent; }
button:focus-visible, input:focus-visible, select:focus-visible {
  outline: 2px solid var(--purple-light);
  outline-offset: 3px;
}
[hidden] { display: none !important; }

/* Entrada, login e cadastro */
#entry {
  min-height: 100vh;
  padding: 22px 20px max(28px, env(safe-area-inset-bottom));
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background:
    radial-gradient(ellipse at 85% 22%, #783bd02b, transparent 38%),
    radial-gradient(ellipse at 8% 90%, #a05cf01a, transparent 32%),
    var(--bg);
}
.entry-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}
.brand {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  color: var(--text);
  font-size: 19px;
  font-weight: 800;
  letter-spacing: -.4px;
}
.brand-mark {
  display: grid;
  width: 38px;
  height: 38px;
  place-items: center;
  background: linear-gradient(140deg, var(--purple), #6f36bc);
  border-radius: 12px;
  font-size: 21px;
}
.entry-content {
  width: 100%;
  max-width: 440px;
  margin: auto;
  padding: 34px 0;
}
.hero-art {
  position: relative;
  display: grid;
  min-height: 215px;
  margin: 0 auto 28px;
  place-items: center;
  isolation: isolate;
}
.hero-glow {
  position: absolute;
  z-index: -1;
  width: 190px;
  height: 190px;
  background: #a05cf02b;
  border-radius: 50%;
  filter: blur(28px);
}
.hero-ring {
  position: absolute;
  width: 185px;
  height: 185px;
  border: 1px solid #bc8af74a;
  border-radius: 50%;
}
.hero-ring::before, .hero-ring::after {
  position: absolute;
  content: "";
  border: 1px solid #bc8af72b;
  border-radius: 50%;
}
.hero-ring::before { inset: 14px; }
.hero-ring::after { inset: 29px; }
.hero-person {
  font-size: 112px;
  line-height: 1;
  filter: drop-shadow(0 10px 24px #a05cf044);
}
.hero-badge {
  position: absolute;
  display: grid;
  width: 46px;
  height: 46px;
  place-items: center;
  background: #211a2d;
  border: 1px solid #684397;
  border-radius: 15px;
  font-size: 22px;
}
.badge-one { top: 29px; right: 12%; transform: rotate(9deg); }
.badge-two { bottom: 25px; left: 12%; transform: rotate(-9deg); }
.entry-screen { animation: appear .24s ease-out; }
@keyframes appear {
  from { opacity: 0; transform: translateY(7px); }
  to { opacity: 1; transform: translateY(0); }
}
.eyebrow {
  margin: 0 0 10px;
  color: var(--purple-light);
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 2px;
  text-align: center;
}
.entry-screen h1 {
  margin: 0;
  font-size: clamp(30px, 8vw, 42px);
  line-height: 1.08;
  letter-spacing: -1.5px;
  text-align: center;
}
.entry-screen h1 span { color: var(--purple-light); }
.entry-copy {
  max-width: 370px;
  margin: 15px auto 27px;
  color: var(--muted);
  font-size: 15px;
  line-height: 1.6;
  text-align: center;
}
.entry-actions { display: grid; gap: 12px; }
.primary-btn, .secondary-btn {
  display: inline-flex;
  min-height: 54px;
  align-items: center;
  justify-content: center;
  padding: 14px 18px;
  border: 1px solid transparent;
  border-radius: 14px;
  font-weight: 800;
  cursor: pointer;
  transition: transform .15s, filter .15s, background .15s;
}
.primary-btn {
  background: linear-gradient(100deg, #8b45dd, var(--purple-light));
  color: #fff;
  box-shadow: 0 8px 26px #8b45dd30;
}
.secondary-btn {
  background: #17141c;
  border-color: #3c3348;
  color: var(--text);
}
.primary-btn:hover, .secondary-btn:hover { filter: brightness(1.09); }
.primary-btn:active, .secondary-btn:active { transform: scale(.99); }
.entry-footer {
  margin: 18px 0 0;
  color: #827c89;
  font-size: 12px;
  line-height: 1.5;
  text-align: center;
}
.auth-card {
  padding: 24px 21px;
  background: #151318eF;
  border: 1px solid #352d3e;
  border-radius: 22px;
  box-shadow: 0 20px 70px #0006;
}
.auth-card h1 {
  font-size: 29px;
  text-align: left;
}
.auth-description {
  margin: 8px 0 20px;
  color: var(--muted);
  font-size: 14px;
  line-height: 1.5;
}
.field { margin: 15px 0; }
.field label {
  display: block;
  margin-bottom: 7px;
  color: #d3ced9;
  font-size: 13px;
  font-weight: 650;
}
.field input {
  width: 100%;
  min-height: 49px;
  padding: 12px 14px;
  background: #0e0d10;
  border: 1px solid #39343e;
  border-radius: 11px;
  color: var(--text);
  font-size: 16px;
}
.field input::placeholder { color: #77717d; }
.password-wrap { position: relative; }
.password-wrap input { padding-right: 55px; }
.password-toggle {
  position: absolute;
  top: 50%;
  right: 8px;
  width: 40px;
  height: 40px;
  transform: translateY(-50%);
  background: none;
  border: 0;
  border-radius: 9px;
  color: var(--muted);
  cursor: pointer;
}
.form-message {
  min-height: 20px;
  margin: 4px 0 10px;
  color: var(--danger);
  font-size: 13px;
  line-height: 1.45;
}
.form-message.success { color: var(--success); }
.form-actions { display: grid; gap: 10px; }
.text-button {
  display: block;
  margin: 12px auto 0;
  padding: 8px;
  background: none;
  border: 0;
  color: var(--purple-light);
  font-size: 14px;
  cursor: pointer;
}
.back-button {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  margin: 0 0 18px;
  padding: 7px 0;
  background: none;
  border: 0;
  color: var(--muted);
  cursor: pointer;
}

/* Aplicativo */
.app-header {
  padding: 22px 18px 18px;
  background: #141414;
  border-bottom: 3px solid var(--purple);
}
.app-header-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}
.app-header h1 { margin: 0; color: var(--purple); font-size: 28px; }
.app-header p { margin: 8px 0 0; font-size: 14px; }
.logout-button {
  padding: 8px 11px;
  background: #211a2d;
  border: 1px solid #49345f;
  border-radius: 10px;
  color: var(--purple-light);
  font-size: 12px;
  font-weight: 700;
  cursor: pointer;
}
nav {
  position: sticky;
  top: 0;
  z-index: 5;
  display: flex;
  background: #1a1a1a;
  border-bottom: 1px solid var(--border);
}
nav button {
  flex: 1;
  padding: 15px 4px;
  background: none;
  border: 0;
  border-bottom: 3px solid transparent;
  color: var(--muted);
  font-size: 12px;
  font-weight: 800;
  letter-spacing: .5px;
  cursor: pointer;
}
nav button.on {
  background: #251f33;
  border-bottom-color: var(--purple);
  color: var(--text);
}
#main { padding: 16px 14px 40px; }
.card {
  margin-bottom: 16px;
  padding: 20px;
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 18px;
}
.workout { cursor: pointer; transition: border-color .2s, box-shadow .2s; }
.workout.selected { border: 2px solid var(--purple); box-shadow: 0 0 22px #a05cf033; }
.icon { margin-bottom: 8px; font-size: 30px; }
.card h2 { margin: 0 0 8px; color: var(--purple-light); font-size: 21px; }
.sequence, .how { color: var(--muted); line-height: 1.5; }
.sequence b, .how b { color: var(--text); }
.meta {
  margin-top: 12px;
  padding-top: 12px;
  border-top: 1px solid var(--border);
  font-size: 14px;
  line-height: 1.8;
}
.foot {
  display: flex;
  flex-wrap: wrap;
  gap: 10px 18px;
  margin-top: 12px;
  padding-top: 14px;
  border-top: 1px solid var(--border);
  color: var(--muted);
  font-size: 14px;
}
.app-btn {
  width: 100%;
  padding: 15px 16px;
  background: linear-gradient(90deg, var(--purple), var(--purple-light));
  border: 0;
  border-radius: 12px;
  color: #fff;
  font-size: 15px;
  font-weight: 800;
  letter-spacing: .4px;
  cursor: pointer;
}
.start { margin-top: 14px; }
.search {
  width: 100%;
  margin: 0 0 14px;
  padding: 13px 14px;
  background: #0f0f0f;
  border: 1px solid var(--border);
  border-radius: 10px;
  color: var(--text);
  font-size: 16px;
}
.exercise { display: flex; gap: 15px; }
.thumb {
  flex: none;
  display: grid;
  width: 58px;
  height: 58px;
  place-items: center;
  background: #0f0f0f;
  border-radius: 12px;
  font-size: 29px;
}
.how { margin: 0; }
.steps {
  margin-top: 12px;
  padding-top: 12px;
  border-top: 1px solid var(--border);
  font-size: 14px;
  line-height: 1.7;
}
.chips {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 10px;*
# Fiel---Fitness
Aplicativo desenvolvido para auxiliar na prática de exercícios físicos, oferecendo uma plataforma moderna e intuitiva para organizar treinos, consultar exercícios e acompanhar a evolução. Seu objetivo é incentivar hábitos saudáveis, promover qualidade de vida e motivar os usuários a alcançarem seus objetivos, respeitando seu próprio ritmo.
