<!DOCTYPE html>

<html lang="ko">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1" name="viewport"/>
<title>Prompt Directory : 250911 업데이트</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&amp;display=swap" rel="stylesheet"/>
<style>
:root{
  --bg:#fffdf8;
  --panel:#fff;
  --sidebar:#f6f1e6;
  --text:#111;
  --muted:#6b7280;
  --brand:#111;
  --border:rgba(17,17,17,.08);
  --code:#faf6ef;
}
*{box-sizing:border-box}
html,body{margin:0;padding:0}
body{background:var(--bg);color:var(--text);font-family:Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, Apple Color Emoji, Segoe UI Emoji;line-height:1.6}
a{color:inherit;text-decoration:none}
/* Layout */
.sidebar{position:fixed;left:0;top:0;height:100vh;width:300px;background:var(--sidebar);border-right:1px solid var(--border);padding:20px 14px;overflow:auto}
.logo{display:flex;align-items:center;gap:10px;font-weight:600;margin-bottom:12px}
.logo .dot{width:18px;height:18px;border-radius:6px;background:linear-gradient(135deg,#ff6b6b,#f59e0b)}
.search{position:sticky;top:0;background:var(--sidebar);padding:8px 0 10px}
.navcat{font-size:11px;font-weight:700;color:#667085;margin:16px 10px 6px}
.nav a{display:block;font-size:13px;padding:8px 10px;border-radius:10px;margin:2px 6px}
.nav a:hover{background:rgba(17,17,17,.06)}
.nav a.active{background:var(--brand);color:#fff}
main{margin-left:300px;padding:24px 40px;max-width:1200px}
header.sticky{position:sticky;top:0;background:linear-gradient(180deg,rgba(255,253,248,.95),rgba(255,253,248,.85));backdrop-filter:saturate(180%) blur(8px);z-index:5;padding:16px 0;border-bottom:1px solid var(--border)}
header h1{margin:0 0 2px 0;font-size:28px;font-weight:800}
header p{margin:0;color:var(--muted);font-size:14px}
/* Section */
.section{padding:28px 0;border-bottom:1px solid var(--border);scroll-margin-top:96px}
.section h3{margin:0 0 8px 0;font-size:24px;font-weight:800}
.section h3 span{font-size:12px;color:#9ca3af;font-weight:600}
.section .desc{margin:0 0 14px 0;color:#374151;font-size:14px}
/* Prompt block */
.prompt{background:var(--panel);border:1px solid var(--border);border-radius:14px;padding:10px;box-shadow:0 1px 0 rgba(17,17,17,.03)}
.prompt-head{display:flex;justify-content:space-between;align-items:center;padding:6px 8px;border-radius:10px;background:rgba(17,17,17,.03);font-size:13px;font-weight:600}
.prompt pre{margin:8px 6px 6px 6px;background:var(--code);padding:12px;border-radius:10px;overflow:auto;font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-size:12px;line-height:1.5}
.copy{border:1px solid var(--border);background:#fff;border-radius:8px;padding:6px 10px;font-size:12px;cursor:pointer}
.copy:hover{background:#f3f4f6}
/* Utilities */
::-webkit-scrollbar{width:10px;height:10px}
::-webkit-scrollbar-thumb{background:rgba(17,17,17,.13);border-radius:8px}
::-webkit-scrollbar-track{background:transparent}
@media (max-width: 960px){
  .sidebar{position:static;width:auto;height:auto}
  main{margin-left:0;padding:16px}
}

/* --- Content refinement --- */
main{max-width:1080px}
.section{padding:40px 0 32px;border-bottom:1px solid var(--border)}
.section h3{font-size:26px;font-weight:800;margin:0 0 10px}
.section h3 span{font-size:12px;color:#9aa1a9;font-weight:600}
.section .desc{margin:0 0 18px 0;color:#2f343a;font-size:15px;line-height:1.7}

/* Card container to match original's beige panel style */
.card{background:#fff; border:1px solid rgba(17,17,17,.06); border-radius:16px; box-shadow:0 1px 0 rgba(17,17,17,.03); overflow:hidden}
.card-head{display:flex; align-items:center; justify-content:space-between; gap:8px; padding:12px 14px; background:#fbf9f4; border-bottom:1px solid rgba(17,17,17,.06)}
.card-head .title{font-size:13px; font-weight:700; color:#3b3f45}
.card-head .actions{display:flex; gap:8px}
.iconbtn{display:inline-flex; align-items:center; gap:6px; padding:6px 10px; border:1px solid rgba(17,17,17,.08); border-radius:10px; background:#fff; font-size:12px; cursor:pointer}
.iconbtn:hover{background:#f5f6f7}
.iconbtn svg{width:14px; height:14px}

/* Code block closer to original */
pre{margin:0; background:#fff; padding:16px 18px; font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; font-size:12.5px; line-height:1.65; white-space:pre-wrap}
/* Subtle highlight for backticks and paths (optional minimal syntax) */
pre em{font-style:normal; color:#6b7280}

/* Improve vertical rhythm */
.section .card{margin-top:8px}
@media (min-width: 1100px){
  .section .card{margin-top:10px}
}

</style>
</head>
<body>
<aside class="sidebar" id="sidebar">
<div class="logo"><div class="dot"></div><div>Prompt Directory</div></div>
<div class="search">
<input id="q" placeholder="검색(영문 제목)" style="width:100%;padding:10px 12px;border:1px solid var(--border);border-radius:10px;background:#fff;outline:none;font-size:13px" type="search"/>
</div>
<nav class="nav" id="nav">
<div class="navcat">FOUNDATION</div>
<a data-target="s1" href="#s1">1. Authentication Flow</a>
<a data-target="s2" href="#s2">2. Google OAuth Login</a>
<a data-target="s3" href="#s3">3. Magic Link Login</a>
<a data-target="s4" href="#s4">4. Role-Based Access Control</a>
<a data-target="s5" href="#s5">5. User Settings Page</a>
<div class="navcat">CORE UX &amp; UI</div>
<a data-target="s6" href="#s6">6. Linear-Style To-Do App</a>
<a data-target="s7" href="#s7">7. Mercury-Style Finance Dashboard</a>
<a data-target="s8" href="#s8">8. Liquid Glass Component System</a>
<a data-target="s9" href="#s9">9. File Upload + Storage</a>
<a data-target="s10" href="#s10">10. Realtime Sync</a>
<a data-target="s11" href="#s11">11. CSV Import &amp; Export</a>
<a data-target="s12" href="#s12">12. Dark Mode Toggle</a>
<div class="navcat">COLLABORATION &amp; GROWTH</div>
<a data-target="s13" href="#s13">13. Team Workspaces</a>
<a data-target="s14" href="#s14">14. Invite System with Links</a>
<a data-target="s15" href="#s15">15. Notification System</a>
<a data-target="s16" href="#s16">16. Email Notifications on Events</a>
<a data-target="s17" href="#s17">17. Push Notifications</a>
<a data-target="s18" href="#s18">18. Audit Logs</a>
<a data-target="s19" href="#s19">19. Activity Feed</a>
<div class="navcat">MONETIZATION</div>
<a data-target="s20" href="#s20">20. Stripe Subscriptions</a>
<a data-target="s21" href="#s21">21. Stripe One-Time Checkout</a>
<a data-target="s22" href="#s22">22. Stripe Usage-Based Billing</a>
<a data-target="s23" href="#s23">23. PayPal Checkout</a>
<a data-target="s24" href="#s24">24. Pro Plan Upgrade</a>
<div class="navcat">INTEGRATIONS</div>
<a data-target="s25" href="#s25">25. Resend Email Integration</a>
<a data-target="s26" href="#s26">26. Twilio SMS Notifications</a>
<a data-target="s27" href="#s27">27. Slack Webhook Notifications</a>
<a data-target="s28" href="#s28">28. Google Maps Autocomplete</a>
<a data-target="s29" href="#s29">29. Calendly API Integration</a>
<a data-target="s30" href="#s30">30. Zapier Integration</a>
<a data-target="s31" href="#s31">31. GitHub OAuth</a>
<a data-target="s32" href="#s32">32. Notion Sync</a>
<div class="navcat">ADVANCED SYSTEMS</div>
<a data-target="s33" href="#s33">33. Admin Analytics Dashboard</a>
<a data-target="s34" href="#s34">34. Event Tracking</a>
<a data-target="s35" href="#s35">35. A/B Testing Framework</a>
<a data-target="s36" href="#s36">36. Feature Flags</a>
<a data-target="s37" href="#s37">37. Rate Limiting Middleware</a>
<a data-target="s38" href="#s38">38. Background Jobs</a>
<a data-target="s39" href="#s39">39. API Key Management</a>
<a data-target="s40" href="#s40">40. Export to PDF</a>
<div class="navcat">AI SUPERPOWERS</div>
<a data-target="s41" href="#s41">41. OpenAI Chatbot Widget</a>
<a data-target="s42" href="#s42">42. AI Content Generator</a>
<a data-target="s43" href="#s43">43. AI Image Generator</a>
<a data-target="s44" href="#s44">44. AI Semantic Search</a>
<a data-target="s45" href="#s45">45. AI Recommendation Engine</a>
<a data-target="s46" href="#s46">46. AI Form Autocomplete</a>
</nav>
</aside>
<main>
<header class="sticky">
  <h1>Prompt Directory : 250911 업데이트</h1>
  <p style="font-size:12px;color:#6b7280">
    <a href="https://prompt-directory-fh.lovable.app/" target="_blank" style="color:#6b7280;text-decoration:underline">
      https://prompt-directory-fh.lovable.app/
    </a>
  </p>
  <p>원문 저작권은 해당 소유자에게 있으며, 이 문서는 학습/참고 목적으로 제공된 번역본입니다.</p>
</header>















































<section class="mb-20 scroll-mt-24" id="s1">
<h3 class="text-2xl font-semibold mb-2">1. 인증 플로우 <span class="text-xs text-gray-500">(Authentication Flow)</span></h3>
<p class="text-sm text-gray-700 mb-3">Supabase로 이메일+비밀번호 인증을 추가합니다. 로그인, 회원가입, 비밀번호 재설정, 보호된 대시보드를 포함합니다.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p1"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p1">Add authentication with Supabase to my Lovable app.
Requirements:
– Frontend: login, signup, and forgot password pages with clean minimal styling (Inter font, –6 letter spacing, greys + blues).
– Backend: Supabase Auth (email + password).
– Add protected route `/dashboard` visible only to logged-in users.
– Store user profiles in `profiles (id, email, role, created_at)`.
– Show error + success states with smooth micro-animations.
– Output: working auth flow integrated with Supabase, responsive, production-ready.</pre></div></section><section class="mb-20 scroll-mt-24" id="s2">
<h3 class="text-2xl font-semibold mb-2">2. Google OAuth 로그인 <span class="text-xs text-gray-500">(Google OAuth Login)</span></h3>
<p class="text-sm text-gray-700 mb-3">Google 계정으로 로그인하도록 설정하고, Supabase에 프로필 정보를 저장합니다.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p2"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p2">Add Google OAuth login to my Lovable app.
Requirements:
– Use Supabase Auth with Google provider.
– Frontend: "Sign in with Google" button (Inter font, –6 letter spacing, greys + blues).
– On success: store user profile in `profiles (id, email, full_name, avatar_url)`.
– Create `/login` page and redirect to `/dashboard` after sign-in.
– Handle errors and loading states with clean micro-animations.
– Output: fully functional Google login flow, styled premium, responsive.</pre></div></section><section class="mb-20 scroll-mt-24" id="s3">
<h3 class="text-2xl font-semibold mb-2">3. 매직 링크 로그인(비밀번호 없음) <span class="text-xs text-gray-500">(Magic Link Login (Passwordless))</span></h3>
<p class="text-sm text-gray-700 mb-3">이메일 매직 링크를 통한 비밀번호 없는 로그인.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p3"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p3">Implement passwordless login with Supabase magic links.
Requirements:
– Configure Supabase Auth for magic link login.
– Frontend: email input + "Send Magic Link" button (Inter font, –6 letter spacing, greys + blues).
– Show confirmation message: "Check your email."
– Auto-redirect back to `/dashboard` after link click.
– Store user profiles in Supabase `profiles` table.
– Output: complete passwordless login flow, copy-paste ready.</pre></div></section><section class="mb-20 scroll-mt-24" id="s4">
<h3 class="text-2xl font-semibold mb-2">4. 역할 기반 접근 제어(RBAC) <span class="text-xs text-gray-500">(Role-Based Access Control (RBAC))</span></h3>
<p class="text-sm text-gray-700 mb-3">역할(관리자, 사용자, 게스트)에 따라 라우트와 UI를 제한합니다.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p4"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p4">Add role-based access control to my Lovable app.
Requirements:
– Supabase schema: `profiles (id, email, role [admin|user|guest])`.
– Protect `/admin` route so only `role=admin` users can access.
– Frontend: conditionally render nav items based on role.
– Create a simple admin dashboard to assign roles.
– Show "Access Denied" message for unauthorized users.
– Output: complete RBAC system with routes and UI protection.</pre></div></section><section class="mb-20 scroll-mt-24" id="s5">
<h3 class="text-2xl font-semibold mb-2">5. 사용자 설정 페이지 <span class="text-xs text-gray-500">(User Settings Page)</span></h3>
<p class="text-sm text-gray-700 mb-3">아바타·이름·환경설정을 관리하는 프로필 페이지.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p5"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p5">Create a user settings page in my Lovable app.
Requirements:
– Features: upload profile picture (stored in Supabase storage), update name, email, and password.
– Add dark/light mode toggle.
– Save preferences in `profiles` table.
– UI: clean Inter font, –6 letter spacing, mobile-first, responsive.
– Show save success + error states with micro-animations.
– Output: full user settings page with persistent data, copy-paste ready.</pre></div></section><section class="mb-20 scroll-mt-24" id="s6">
<h3 class="text-2xl font-semibold mb-2">6. Linear 스타일 To-Do 앱 <span class="text-xs text-gray-500">(Linear-Style To-Do App)</span></h3>
<p class="text-sm text-gray-700 mb-3">Supabase에 영속 저장하는 미니멀 To-Do 앱.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p6"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p6">Create a Linear-inspired To-Do app.
Requirements:
– Components: task list, add task input, tag selector, complete/undo toggle.
– Supabase schema: `tasks (id, title, tags, completed)`.
– All tasks shown in a clean home view with hover states + animations (scale-105 on hover).
– Mobile-first layout with responsive bottom nav bar.
– Output: polished to-do system with CRUD operations, intuitive UX.</pre></div></section><section class="mb-20 scroll-mt-24" id="s7">
<h3 class="text-2xl font-semibold mb-2">7. Mercury 스타일 금융 대시보드 <span class="text-xs text-gray-500">(Mercury-Style Finance Dashboard)</span></h3>
<p class="text-sm text-gray-700 mb-3">잔액·거래·차트를 포함한 프리미엄 금융 대시보드.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p7"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p7">Design a Mercury-inspired finance dashboard.
Requirements:
– Inter font, –6 spacing, minimal black/grey with subtle blue highlights.
– Modules: balance card, recent transactions table, graph for cash flow, side nav.
– Supabase schema: `accounts (id, name, balance)`, `transactions (id, account_id, amount, type, date)`.
– Live data binding: balances auto-update after new transactions.
– Add filters: "Last 7 days / 30 days / All time."
– Micro-interactions: fade-in charts, ripple on buttons.
– Output: fully functional dashboard with seeded test data.</pre></div></section><section class="mb-20 scroll-mt-24" id="s8">
<h3 class="text-2xl font-semibold mb-2">8. Liquid Glass 컴포넌트 시스템 <span class="text-xs text-gray-500">(Liquid Glass Component System)</span></h3>
<p class="text-sm text-gray-700 mb-3">Apple VisionOS 느낌의 글래시 UI 컴포넌트.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p8"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p8">Create a "Liquid Glass" component set.
Requirements:
– UI: bg-white/10 → bg-white/20, backdrop-blur-md, iridescent gradient borders, shadow-xl, rounded-2xl.
– Components: nav bar, toggle switch, feature card, tab menu.
– Micro-interactions: scale-105 hover, ripple click, shimmer cursor effect.
– White + dark mode support.
– Inter font (–6 spacing) across all components.
– Output: clean React/TS components styled with Tailwind, ready to drop into Lovable.</pre></div></section><section class="mb-20 scroll-mt-24" id="s9">
<h3 class="text-2xl font-semibold mb-2">9. 파일 업로드 + 스토리지 <span class="text-xs text-gray-500">(File Upload + Storage)</span></h3>
<p class="text-sm text-gray-700 mb-3">Supabase 스토리지를 사용해 파일 업로드·미리보기·관리.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p9"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p9">Add file upload and storage to my Lovable app.
Requirements:
– Frontend: upload button + drag-and-drop zone with progress bar.
– Store files in Supabase storage bucket `uploads`.
– Generate signed URLs for secure file retrieval.
– List uploaded files with delete option.
– Mobile responsive, Inter –6, greys + blues.
– Output: complete working upload flow, copy-paste ready.</pre></div></section><section class="mb-20 scroll-mt-24" id="s10">
<h3 class="text-2xl font-semibold mb-2">10. 실시간 동기화(채팅 예시) <span class="text-xs text-gray-500">(Realtime Sync (Chat Example))</span></h3>
<p class="text-sm text-gray-700 mb-3">Supabase 구독을 이용한 실시간 채팅.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p10"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p10">Add realtime updates to my Lovable app.
Requirements:
– Subscribe to changes in `messages` table.
– Frontend: chat component that updates instantly when new rows inserted.
– Smooth fade-in for new messages.
– Support mobile view with fixed input bar.
– Output: working realtime chat component.</pre></div></section><section class="mb-20 scroll-mt-24" id="s11">
<h3 class="text-2xl font-semibold mb-2">11. CSV 가져오기 &amp; 내보내기 <span class="text-xs text-gray-500">(CSV Import &amp; Export)</span></h3>
<p class="text-sm text-gray-700 mb-3">CSV로 Supabase에 데이터를 쉽게 주고받기.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p11"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p11">Add CSV import/export to my Lovable app.
Requirements:
– Frontend: file upload → parse CSV → insert rows into Supabase table `contacts`.
– Export: download table rows back to CSV.
– Progress bar + error handling.
– Store import logs in `imports` table.
– Output: full CSV import/export workflow with UI.</pre></div></section><section class="mb-20 scroll-mt-24" id="s12">
<h3 class="text-2xl font-semibold mb-2">12. 다크 모드 토글 <span class="text-xs text-gray-500">(Dark Mode Toggle)</span></h3>
<p class="text-sm text-gray-700 mb-3">사용자 프로필에 테마를 저장하는 라이트/다크 모드.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p12"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p12">Add a dark/light mode toggle to my Lovable app.
Requirements:
– UI toggle button in settings or nav bar.
– Persist preference in `profiles` table.
– Apply dark classes globally with Tailwind.
– Output: persistent dark mode system across sessions.</pre></div></section><section class="mb-20 scroll-mt-24" id="s13">
<h3 class="text-2xl font-semibold mb-2">13. 팀 워크스페이스(멀티 테넌시) <span class="text-xs text-gray-500">(Team Workspaces (Multi-Tenant))</span></h3>
<p class="text-sm text-gray-700 mb-3">조직 멤버십·역할·워크스페이스 전환을 지원.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p13"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p13">Add team workspaces to my Lovable app.
Requirements:
– Supabase schema: `organizations (id, name)`, `memberships (id, org_id, user_id, role)`.
– Users can create orgs, invite members, and switch between orgs.
– Frontend: org switcher in sidebar.
– Routes and data scoped to current org.
– Output: fully working multi-tenant workspace system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s14">
<h3 class="text-2xl font-semibold mb-2">14. 링크 초대 시스템 <span class="text-xs text-gray-500">(Invite System with Links)</span></h3>
<p class="text-sm text-gray-700 mb-3">만료되는 초대 링크로 신규 사용자가 조직에 참여.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p14"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p14">Add invite system with unique links to my Lovable app.
Requirements:
– Backend: generate signed invite links (expire in 7 days).
– Supabase table `invites (id, org_id, email, token, expires_at)`.
– Frontend: input email → send invite via Resend email.
– Accepting invite auto-joins user as member.
– Output: working invite + acceptance flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s15">
<h3 class="text-2xl font-semibold mb-2">15. 알림 시스템 <span class="text-xs text-gray-500">(Notification System)</span></h3>
<p class="text-sm text-gray-700 mb-3">앱 전역 알림 드롭다운과 읽지 않음 배지.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p15"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p15">Add a notification system to my Lovable app.
Requirements:
– Supabase schema: `notifications (id, user_id, message, read, created_at)`.
– Frontend: bell icon in nav bar with dropdown.
– Unread count badge (blue).
– Clicking marks notification as read and fades it out.
– Micro-interactions: fade + slide transitions.
– Output: end-to-end notification system, styled premium.</pre></div></section><section class="mb-20 scroll-mt-24" id="s16">
<h3 class="text-2xl font-semibold mb-2">16. 이벤트 이메일 알림 <span class="text-xs text-gray-500">(Email Notifications on Events)</span></h3>
<p class="text-sm text-gray-700 mb-3">이벤트 발생 시 Resend 이메일 발송(예: 가입).</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p16"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p16">Trigger emails on app events in my Lovable app.
Requirements:
– Example: new signup → send welcome email via Resend.
– Backend function `/api/send-welcome` called after profile insert.
– Store email logs in `email_logs` table.
– Output: end-to-end event → email notification system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s17">
<h3 class="text-2xl font-semibold mb-2">17. 푸시 알림(PWA) <span class="text-xs text-gray-500">(Push Notifications (PWA))</span></h3>
<p class="text-sm text-gray-700 mb-3">백엔드 이벤트로 브라우저 푸시 알림.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p17"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p17">Add browser push notifications to my Lovable app.
Requirements:
– Use service worker to subscribe users.
– Backend: `/api/notify` sends push payloads.
– Supabase table `push_subscriptions`.
– Trigger push on events (e.g., new message).
– Output: working push notification system in PWA app.</pre></div></section><section class="mb-20 scroll-mt-24" id="s18">
<h3 class="text-2xl font-semibold mb-2">18. 감사 로그 <span class="text-xs text-gray-500">(Audit Logs)</span></h3>
<p class="text-sm text-gray-700 mb-3">데이터베이스 변경 이력을 추적.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p18"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p18">Add audit logging to my Lovable app.
Requirements:
– Supabase table `audit_logs (id, user_id, action, table, row_id, created_at)`.
– Automatically log inserts/updates/deletes via triggers.
– Admin dashboard to view logs (table with filters).
– Output: complete logging system with UI.</pre></div></section><section class="mb-20 scroll-mt-24" id="s19">
<h3 class="text-2xl font-semibold mb-2">19. 활동 피드 <span class="text-xs text-gray-500">(Activity Feed)</span></h3>
<p class="text-sm text-gray-700 mb-3">GitHub 스타일의 활동 타임라인.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p19"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p19">Add an activity feed to my Lovable app.
Requirements:
– Supabase schema: `activities (id, user_id, action, target, created_at)`.
– Timeline view grouped by day.
– Micro-interactions: slide-in on new activity.
– Output: fully working activity feed with live data.</pre></div></section><section class="mb-20 scroll-mt-24" id="s20">
<h3 class="text-2xl font-semibold mb-2">20. Stripe 구독 <span class="text-xs text-gray-500">(Stripe Subscriptions)</span></h3>
<p class="text-sm text-gray-700 mb-3">Stripe Checkout을 통한 반복 구독 플로우.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p20"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p20">Add Stripe subscriptions to my Lovable app.
Requirements:
– Backend: API route `/api/checkout` initializes $20/month subscription session.
– Use Stripe SDK with keys from env vars.
– Frontend: Subscribe button → calls API → redirects to Stripe Checkout.
– Webhook updates Supabase `users` table with `is_pro`.
– Add confirmation page `/success`.
– Output: end-to-end Stripe subscription flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s21">
<h3 class="text-2xl font-semibold mb-2">21. Stripe 일회성 결제 <span class="text-xs text-gray-500">(Stripe One-Time Checkout)</span></h3>
<p class="text-sm text-gray-700 mb-3">일회성 구매(Stripe) 플로우.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p21"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p21">Add a one-time product checkout to my Lovable app.
Requirements:
– Backend: API route `/api/checkout` creates Checkout Session for $49 product.
– Frontend: "Buy Now" button → calls API → redirects to Stripe.
– Webhook `/api/webhook` updates Supabase `orders (id, user_id, status, amount)`.
– Confirmation page `/success`.
– Output: full Stripe one-time checkout flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s22">
<h3 class="text-2xl font-semibold mb-2">22. Stripe 사용량 기반 과금 <span class="text-xs text-gray-500">(Stripe Usage-Based Billing)</span></h3>
<p class="text-sm text-gray-700 mb-3">사용량(예: API 호출)에 기반하여 과금.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p22"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p22">Add usage-based billing to my Lovable app.
Requirements:
– Backend: create subscription with Stripe metered plan.
– Track usage events and report to Stripe's usage API.
– Supabase table `usage (id, user_id, event, count, created_at)`.
– Admin dashboard shows current usage + bill estimate.
– Output: full integration with Stripe metered billing.</pre></div></section><section class="mb-20 scroll-mt-24" id="s23">
<h3 class="text-2xl font-semibold mb-2">23. PayPal 결제 <span class="text-xs text-gray-500">(PayPal Checkout)</span></h3>
<p class="text-sm text-gray-700 mb-3">대체 결제 수단으로 PayPal 제공.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p23"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p23">Offer PayPal as an alternative checkout method.
Requirements:
– Integrate PayPal JS SDK with client ID in env vars.
– Frontend: PayPal button (minimal styling).
– On success: create `orders` row in Supabase.
– Redirect user to confirmation page.
– Include error handling + loading spinner.
– Output: working PayPal integration alongside Stripe.</pre></div></section><section class="mb-20 scroll-mt-24" id="s24">
<h3 class="text-2xl font-semibold mb-2">24. Pro 플랜 업그레이드(일할 계산) <span class="text-xs text-gray-500">(Pro Plan Upgrade (Pro-Rata))</span></h3>
<p class="text-sm text-gray-700 mb-3">명확한 일할 계산으로 업그레이드 비용 안내.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p24"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p24">Add an upgrade flow with pro-rata billing to my Lovable app.
Requirements:
– Stripe integration: calculate pro-rata fee when upgrading plan.
– UI should explain clearly: "Pay only the difference today."
– Show current plan → new plan → today's charge.
– Update user in Supabase to `is_pro`.
– Output: transparent, user-friendly upgrade experience.</pre></div></section><section class="mb-20 scroll-mt-24" id="s25">
<h3 class="text-2xl font-semibold mb-2">25. Resend 이메일 연동 <span class="text-xs text-gray-500">(Resend Email Integration)</span></h3>
<p class="text-sm text-gray-700 mb-3">Resend로 트랜잭션 이메일 발송.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p25"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p25">Integrate Resend email sending into my Lovable app.
Requirements:
– Utility function `sendEmail(to: string, subject: string, html: string)`.
– Store API key in env vars.
– Create API route `/api/test-email` that sends a sample email.
– Add error handling, logging, and success response.
– Output: clean, copy-paste code (TypeScript + edge API endpoint).</pre></div></section><section class="mb-20 scroll-mt-24" id="s26">
<h3 class="text-2xl font-semibold mb-2">26. Twilio SMS 알림 <span class="text-xs text-gray-500">(Twilio SMS Notifications)</span></h3>
<p class="text-sm text-gray-700 mb-3">Twilio를 통한 SMS 발송.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p26"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p26">Integrate Twilio SMS into my Lovable app.
Requirements:
– Backend API `/api/send-sms` using Twilio SDK.
– Env vars for Twilio SID + token.
– Function `sendSMS(to, message)` to send SMS.
– Frontend: simple form (phone number, message, "Send" button).
– Store SMS logs in `sms_logs (id, to, message, status, created_at)`.
– Output: complete Twilio SMS integration with testable flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s27">
<h3 class="text-2xl font-semibold mb-2">27. Slack 웹훅 알림 <span class="text-xs text-gray-500">(Slack Webhook Notifications)</span></h3>
<p class="text-sm text-gray-700 mb-3">가입 등 이벤트를 Slack 채널로 전송.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p27"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p27">Integrate Slack notifications into my Lovable app.
Requirements:
– Backend: API route `/api/notify-slack` posts to Slack webhook URL.
– Example: new signup → posts user email to Slack.
– Env var for Slack webhook URL.
– Supabase trigger: on new `profiles` row, call webhook.
– Output: end-to-end Slack integration with example event.</pre></div></section><section class="mb-20 scroll-mt-24" id="s28">
<h3 class="text-2xl font-semibold mb-2">28. Google Maps 자동완성 + 임베드 <span class="text-xs text-gray-500">(Google Maps Autocomplete + Embed)</span></h3>
<p class="text-sm text-gray-700 mb-3">주소 자동완성 및 지도 표시.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p28"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p28">Add Google Maps autocomplete + embed to my Lovable app.
Requirements:
– Frontend: address input with autocomplete dropdown.
– On selection: save structured address to Supabase `locations`.
– Display selected location on embedded map below input.
– Env var for Maps API key.
– Responsive, Inter –6 spacing.
– Output: fully working location picker flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s29">
<h3 class="text-2xl font-semibold mb-2">29. Calendly API 연동 <span class="text-xs text-gray-500">(Calendly API Integration)</span></h3>
<p class="text-sm text-gray-700 mb-3">예약 정보를 가져와 표시.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p29"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p29">Integrate Calendly bookings into my Lovable app.
Requirements:
– Backend: fetch bookings via Calendly API.
– Supabase schema: `bookings (id, user_id, event_name, date, attendee_email)`.
– Frontend dashboard widget showing upcoming events.
– Auto-sync bookings every hour (edge cron).
– Output: working booking sync + dashboard component.</pre></div></section><section class="mb-20 scroll-mt-24" id="s30">
<h3 class="text-2xl font-semibold mb-2">30. Zapier 연동 <span class="text-xs text-gray-500">(Zapier Integration)</span></h3>
<p class="text-sm text-gray-700 mb-3">앱 이벤트로 Zapier 자동화 트리거.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p30"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p30">Add Zapier webhook integration to my Lovable app.
Requirements:
– Backend: create `/api/webhook` endpoint.
– On new Supabase `profiles` row, send webhook to Zapier.
– Example Zap: new signup → Google Sheets row.
– Use env var for Zapier webhook URL.
– Output: working Zapier integration for automations.</pre></div></section><section class="mb-20 scroll-mt-24" id="s31">
<h3 class="text-2xl font-semibold mb-2">31. GitHub OAuth + 저장소 뷰어 <span class="text-xs text-gray-500">(GitHub OAuth + Repo Viewer)</span></h3>
<p class="text-sm text-gray-700 mb-3">GitHub 로그인 및 저장소 보기.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p31"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p31">Add GitHub OAuth + repo viewer to my Lovable app.
Requirements:
– GitHub OAuth login flow.
– On success: fetch user repos from GitHub API.
– Store user in Supabase.
– Frontend: dashboard list of repos with latest commits.
– Output: GitHub integration with OAuth + repo display.</pre></div></section><section class="mb-20 scroll-mt-24" id="s32">
<h3 class="text-2xl font-semibold mb-2">32. Notion 동기화 <span class="text-xs text-gray-500">(Notion Sync)</span></h3>
<p class="text-sm text-gray-700 mb-3">Notion의 작업/문서를 Supabase와 동기화.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p32"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p32">Add Notion API sync to my Lovable app.
Requirements:
– Fetch notes/tasks from a Notion database using official API.
– Supabase schema: `notion_items (id, title, type, content, last_synced)`.
– Frontend: list synced docs with search + filter.
– Sync every hour with edge cron.
– Output: Notion → Lovable sync with dashboard.</pre></div></section><section class="mb-20 scroll-mt-24" id="s33">
<h3 class="text-2xl font-semibold mb-2">33. 관리자 분석 대시보드 <span class="text-xs text-gray-500">(Admin Analytics Dashboard)</span></h3>
<p class="text-sm text-gray-700 mb-3">가입자·활성 사용자·매출을 추적.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p33"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p33">Add an admin analytics dashboard to my Lovable app.
Requirements:
– Charts: user signups, active users, revenue (from orders table).
– Filters: 7d, 30d, All time.
– Responsive card layout, Inter –6 spacing.
– Output: polished admin analytics dashboard with real data.</pre></div></section><section class="mb-20 scroll-mt-24" id="s34">
<h3 class="text-2xl font-semibold mb-2">34. 이벤트 트래킹(분석) <span class="text-xs text-gray-500">(Event Tracking (Analytics))</span></h3>
<p class="text-sm text-gray-700 mb-3">프론트엔드 행동을 기록하고 통계를 확인.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p34"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p34">Add event tracking to my Lovable app.
Requirements:
– Supabase schema: `events (id, user_id, event, metadata, created_at)`.
– Utility function `trackEvent(event, metadata)` callable from anywhere.
– Track page views + button clicks.
– Dashboard with charts for top events (Recharts).
– Output: complete event tracking system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s35">
<h3 class="text-2xl font-semibold mb-2">35. A/B 테스트 프레임워크 <span class="text-xs text-gray-500">(A/B Testing Framework)</span></h3>
<p class="text-sm text-gray-700 mb-3">변형 실험을 수행하고 전환을 추적.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p35"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p35">Add A/B testing to my Lovable app.
Requirements:
– Supabase table `experiments (id, name, variant, user_id)`.
– Randomly assign users to variant A or B.
– Frontend: render different UI based on variant.
– Log conversions.
– Dashboard: compare results A vs B.
– Output: complete feature testing workflow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s36">
<h3 class="text-2xl font-semibold mb-2">36. 기능 플래그 <span class="text-xs text-gray-500">(Feature Flags)</span></h3>
<p class="text-sm text-gray-700 mb-3">기능을 동적으로 켜고 끄기.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p36"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p36">Add feature flags to my Lovable app.
Requirements:
– Supabase table `feature_flags (id, key, enabled)`.
– Frontend utility `isFeatureEnabled(key)`.
– Admin UI to toggle features.
– Conditional rendering of new components.
– Output: complete feature flagging system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s37">
<h3 class="text-2xl font-semibold mb-2">37. 리밋 미들웨어 <span class="text-xs text-gray-500">(Rate Limiting Middleware)</span></h3>
<p class="text-sm text-gray-700 mb-3">API 호출을 제한하여 남용 방지.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p37"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p37">Add API rate limiting to my Lovable app.
Requirements:
– Supabase table `rate_limits (id, user_id, count, last_reset)`.
– Middleware to block requests &gt;100/minute per user.
– Reset counter every minute.
– Return error JSON when exceeded.
– Output: production-ready rate limiting system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s38">
<h3 class="text-2xl font-semibold mb-2">38. 백그라운드 작업(크론) <span class="text-xs text-gray-500">(Background Jobs (Cron))</span></h3>
<p class="text-sm text-gray-700 mb-3">주기적 백그라운드 작업을 스케줄링.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p38"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p38">Add background jobs with cron to my Lovable app.
Requirements:
– Supabase Edge Function triggered by cron.
– Example: nightly cleanup of expired invites.
– Log runs in `job_logs (id, job_name, run_at, status)`.
– Output: working background job system with example task.</pre></div></section><section class="mb-20 scroll-mt-24" id="s39">
<h3 class="text-2xl font-semibold mb-2">39. API 키 관리 <span class="text-xs text-gray-500">(API Key Management)</span></h3>
<p class="text-sm text-gray-700 mb-3">사용자용 API 키 발급/회수.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p39"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p39">Add API key management to my Lovable app.
Requirements:
– Supabase schema: `api_keys (id, user_id, key, status)`.
– Functions to generate/revoke keys.
– Middleware to check `x-api-key`.
– Admin dashboard to view/manage keys.
– Output: working API key system.</pre></div></section><section class="mb-20 scroll-mt-24" id="s40">
<h3 class="text-2xl font-semibold mb-2">40. PDF로 내보내기 <span class="text-xs text-gray-500">(Export to PDF)</span></h3>
<p class="text-sm text-gray-700 mb-3">앱 데이터를 브랜드 PDF로 생성.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p40"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p40">Add PDF export to my Lovable app.
Requirements:
– Edge function that generates PDFs with reportlab.
– Supabase: store generated PDFs in `exports` table.
– Frontend: "Export to PDF" button in dashboard.
– Output: working PDF export workflow with storage.</pre></div></section><section class="mb-20 scroll-mt-24" id="s41">
<h3 class="text-2xl font-semibold mb-2">41. OpenAI 챗봇 위젯 <span class="text-xs text-gray-500">(OpenAI Chatbot Widget)</span></h3>
<p class="text-sm text-gray-700 mb-3">GPT-4o/GPT-5 기반 플로팅 챗 위젯.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p41"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p41">Add an OpenAI chatbot widget to my Lovable app.
Requirements:
– Frontend: floating widget bottom-right, minimal grey/blue styling, Inter –6 spacing.
– Backend: `/api/chat` route that streams responses from GPT-4o or GPT-5.
– Use function calling for support context.
– Supabase table `conversations` for persistence.
– Typing indicator + smooth fade-in.
– Output: complete chatbot system with persistence.</pre></div></section><section class="mb-20 scroll-mt-24" id="s42">
<h3 class="text-2xl font-semibold mb-2">42. AI 콘텐츠 생성기 <span class="text-xs text-gray-500">(AI Content Generator)</span></h3>
<p class="text-sm text-gray-700 mb-3">OpenAI로 텍스트 콘텐츠 생성(블로그, 소셜 등).</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p42"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p42">Add an AI content generator to my Lovable app.
Requirements:
– Backend API `/api/generate` using OpenAI.
– Inputs: topic, tone, length.
– Supabase: store drafts in `content_drafts`.
– Frontend: editor with save option.
– Output: working content generator with persistence.</pre></div></section><section class="mb-20 scroll-mt-24" id="s43">
<h3 class="text-2xl font-semibold mb-2">43. AI 이미지 생성기 <span class="text-xs text-gray-500">(AI Image Generator)</span></h3>
<p class="text-sm text-gray-700 mb-3">DALL·E/Stability로 프롬프트 기반 이미지 생성.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p43"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p43">Add an AI image generator to my Lovable app.
Requirements:
– Backend API `/api/generate-image` using DALL·E or Stability API.
– Supabase storage for generated images.
– Frontend: prompt input + image gallery grid.
– Output: working AI image generator flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s44">
<h3 class="text-2xl font-semibold mb-2">44. AI 시맨틱 검색 <span class="text-xs text-gray-500">(AI Semantic Search)</span></h3>
<p class="text-sm text-gray-700 mb-3">임베딩 기반 문서 시맨틱 검색.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p44"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p44">Add semantic search to my Lovable app.
Requirements:
– Store OpenAI embeddings in Supabase vector table.
– Backend API `/api/search` to query semantic results.
– Frontend: search bar with instant results.
– Output: working semantic search system with Supabase vectors.</pre></div></section><section class="mb-20 scroll-mt-24" id="s45">
<h3 class="text-2xl font-semibold mb-2">45. AI 추천 엔진 <span class="text-xs text-gray-500">(AI Recommendation Engine)</span></h3>
<p class="text-sm text-gray-700 mb-3">사용자 행동 기반 개인화 추천.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p45"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p45">Add an AI recommendation system to my Lovable app.
Requirements:
– Backend API `/api/recommend` using OpenAI.
– Input: user activity/events.
– Output: recommended items list.
– Supabase: store recommendations in `recommendations` table.
– Output: personalized recommendation flow.</pre></div></section><section class="mb-20 scroll-mt-24" id="s46">
<h3 class="text-2xl font-semibold mb-2">46. AI 폼 자동완성 <span class="text-xs text-gray-500">(AI Form Autocomplete)</span></h3>
<p class="text-sm text-gray-700 mb-3">폼 입력에 대한 스마트 제안.</p>

<div class="card"><div class="card-head"><div class="title">Prompt (원문)</div><div class="actions"><button aria-label="Copy prompt" class="iconbtn" data-src="p46"><svg fill="none" stroke="currentColor" viewbox="0 0 24 24"><rect height="13" rx="2" ry="2" width="13" x="9" y="9"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg> 복사</button></div></div><pre class="bg-transparent whitespace-pre-wrap text-xs leading-5" id="p46">Add AI-powered form autocomplete to my Lovable app.
Requirements:
– Backend API `/api/autofill` using GPT-4.
– Example: suggest addresses, companies, names.
– Frontend: inline suggestions as user types.
– Output: working smart form filler with AI.</pre></div></section></main>
<script>
// Scrollspy + active state
const links = Array.from(document.querySelectorAll('#sidebar a[data-target]'));
const map = new Map(links.map(a => [a.dataset.target, a]));
function setActive(id){ links.forEach(l=>l.classList.toggle('active', l.dataset.target===id)); }
links.forEach(l => l.addEventListener('click', () => setActive(l.dataset.target)));
const obs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{ if(e.isIntersecting){ setActive(e.target.id);} })
},{rootMargin:'-40% 0px -55% 0px',threshold:0});
document.querySelectorAll('section[id^="s"]').forEach(sec=>obs.observe(sec));

// Search filter (simple contains on English titles)
const q = document.getElementById('q');
q.addEventListener('input', () => {
  const term = q.value.toLowerCase();
  links.forEach(a => {
    const show = a.textContent.toLowerCase().includes(term);
    a.style.display = show ? '' : 'none';
  });
});

// Copy buttons
document.querySelectorAll('.iconbtn').forEach(btn=>{
  btn.addEventListener('click', async ()=>{
    const id = btn.getAttribute('data-src');
    const pre = document.getElementById(id);
    try{
      await navigator.clipboard.writeText(pre.innerText);
      btn.innerHTML='완료';
      setTimeout(()=>btn.innerHTML='<svg viewBox=\'0 0 24 24\' fill=\'none\' stroke=\'currentColor\'><rect x=\'9\' y=\'9\' width=\'13\' height=\'13\' rx=\'2\' ry=\'2\'></rect><path d=\'M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1\'/></svg> 복사',1200);
    }catch(e){
      btn.innerHTML='실패';
      setTimeout(()=>btn.innerHTML='<svg viewBox=\'0 0 24 24\' fill=\'none\' stroke=\'currentColor\'><rect x=\'9\' y=\'9\' width=\'13\' height=\'13\' rx=\'2\' ry=\'2\'></rect><path d=\'M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1\'/></svg> 복사',1200);
    }
  });
});
</script>
</body>
</html>
