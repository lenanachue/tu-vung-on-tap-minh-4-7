<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ôn Tập Từ Vựng Dễ Thương</title>
<style>
:root{
  --purple-1:#f5ebff;
  --purple-2:#e9d5ff;
  --purple-3:#c4b5fd;
  --purple-4:#a78bfa;
  --purple-5:#8b5cf6;
  --purple-dark:#6d28d9;
  --pink:#f5d0fe;
  --card-bg:#ffffff;
  --correct:#4ade80;
  --wrong:#fb7185;
}
*{box-sizing:border-box;}
body{
  margin:0;
  font-family:'Segoe UI','Roboto',Arial,sans-serif;
  background:linear-gradient(135deg,#f5ebff 0%, #ede9fe 45%, #fdf2ff 100%);
  color:#4c1d95;
  min-height:100vh;
  position:relative;
  overflow-x:hidden;
}
.floaty{
  position:fixed;
  font-size:32px;
  opacity:0.2;
  z-index:0;
  animation:float 7s ease-in-out infinite;
  pointer-events:none;
}
@keyframes float{
  0%,100%{transform:translateY(0px) rotate(0deg);}
  50%{transform:translateY(-20px) rotate(10deg);}
}
.f1{top:5%;left:4%;}
.f2{top:15%;right:6%;animation-delay:1.2s;}
.f3{bottom:18%;left:6%;animation-delay:2.4s;}
.f4{bottom:6%;right:8%;animation-delay:1.8s;}
.f5{top:45%;left:2%;animation-delay:3.2s;}
.f6{top:55%;right:3%;animation-delay:2s;}
.f7{top:30%;left:45%;animation-delay:4s;}

.wrap{max-width:920px; margin:0 auto; padding:26px 18px 60px; position:relative; z-index:1;}
header{text-align:center; margin-bottom:16px;}
header h1{
  font-size:clamp(22px,4vw,30px);
  background:linear-gradient(90deg,var(--purple-5),#ec4899);
  -webkit-background-clip:text; background-clip:text; color:transparent;
  margin:0 0 6px;
}
header p{color:#7c3aed; font-size:14.5px; margin:0;}

.theory-box{
  background:#fff;
  border:2px dashed var(--purple-4);
  border-radius:18px;
  padding:16px 18px;
  margin:16px 0 26px;
  font-size:13.5px;
  color:#6d28d9;
  line-height:1.7;
}
.theory-box .title{font-weight:700; color:var(--purple-5); font-size:15px; display:block; margin-bottom:6px;}
.theory-box b{color:#a21caf;}

.tabs{display:flex; flex-wrap:wrap; gap:8px; justify-content:center; margin-bottom:22px;}
.tab-btn{
  border:2px solid var(--purple-3); background:#ffffffaa; color:var(--purple-5);
  padding:10px 16px; border-radius:16px; cursor:pointer; font-weight:600; font-size:13.5px; transition:all .2s;
}
.tab-btn:hover{background:var(--purple-1);}
.tab-btn.active{
  background:linear-gradient(90deg,var(--purple-4),#f0abfc); color:#fff; border-color:transparent;
  box-shadow:0 4px 14px rgba(167,139,250,0.4);
}

.panel{display:none;}
.panel.active{display:block; animation:fadein .35s ease;}
@keyframes fadein{from{opacity:0;transform:translateY(8px);}to{opacity:1;transform:translateY(0);}}

.section-title{
  font-size:18px; color:var(--purple-dark); margin:6px 0 6px;
  padding-left:10px; border-left:5px solid var(--purple-4);
}
.section-sub{font-size:13px; color:#a855f7; margin:0 0 16px 15px; font-style:italic;}

.card{
  background:var(--card-bg); border:2px solid var(--purple-2); border-left:6px solid var(--purple-4);
  border-radius:18px; padding:14px 18px; margin-bottom:12px;
  box-shadow:0 3px 10px rgba(167,139,250,0.1);
  display:flex; gap:12px; align-items:flex-start;
}
.icon-box{
  flex:0 0 44px; height:44px; display:flex; align-items:center; justify-content:center;
  font-size:26px; background:var(--purple-1); border-radius:12px;
}
.icon-box svg{width:28px; height:28px;}
.card-body{flex:1;}
.word-row{display:flex; align-items:baseline; gap:8px; flex-wrap:wrap; margin-bottom:2px;}
.word{font-size:18px; font-weight:700; color:var(--purple-5);}
.ipa{color:#a78bfa; font-size:13.5px;}
.pos{background:var(--purple-1); color:var(--purple-5); font-size:11.5px; padding:2px 7px; border-radius:8px; font-style:italic;}
.meaning{font-size:14.5px; color:#4c1d95; margin:3px 0 6px; font-weight:600;}
.mnemonic{background:#fdf2ff; border:1px dashed var(--purple-3); border-radius:10px; padding:7px 10px; font-size:13px; color:#a21caf;}
.mnemonic b{color:var(--purple-5);}

.cat-grid{display:flex; flex-wrap:wrap; gap:10px; margin-bottom:8px;}
.cat-item{
  background:#fff; border:2px solid var(--purple-2); border-radius:14px;
  padding:8px 12px; display:flex; align-items:center; gap:8px; font-size:14px; font-weight:600; color:#4c1d95;
}
.cat-item select{
  border:1.5px solid var(--purple-3); border-radius:8px; padding:4px 6px; font-size:13px; color:var(--purple-dark); background:var(--purple-1);
}
.cat-item.correct{border-color:var(--correct); background:#f0fdf4;}
.cat-item.wrong{border-color:var(--wrong); background:#fff1f2;}

.sentence-card{
  background:var(--card-bg); border:2px solid var(--purple-2); border-radius:14px;
  padding:13px 16px; margin-bottom:11px; line-height:2; font-size:14.5px;
}
.sentence-card .num{color:var(--purple-4); font-weight:700; margin-right:4px;}
.blank-input{
  border:none; border-bottom:2.5px solid var(--purple-4); background:var(--purple-1);
  padding:3px 8px; font-size:14.5px; font-family:inherit; width:130px; text-align:center;
  border-radius:6px 6px 0 0; color:var(--purple-dark); font-weight:600;
}
.blank-input:focus{outline:none; background:#fff; border-bottom-color:#ec4899;}
.blank-input.correct{background:#f0fdf4; border-bottom-color:var(--correct); color:#15803d;}
.blank-input.wrong{background:#fff1f2; border-bottom-color:var(--wrong); color:#be123c;}
.hint-btn{
  border:1px solid var(--purple-3); background:#fdf2ff; color:var(--purple-5);
  font-size:11.5px; padding:3px 8px; border-radius:10px; cursor:pointer; margin-left:6px;
}
.hint-text{font-size:12px; color:#a855f7; margin-top:5px; display:none;}

.check-row{display:flex; gap:10px; justify-content:center; margin:22px 0 10px; flex-wrap:wrap;}
.btn{border:none; padding:11px 24px; border-radius:14px; font-weight:700; font-size:14.5px; cursor:pointer; transition:transform .15s;}
.btn:hover{transform:translateY(-2px) scale(1.02);}
.btn-primary{background:linear-gradient(90deg,var(--purple-4),#ec4899); color:#fff; box-shadow:0 4px 12px rgba(167,139,250,0.4);}
.btn-secondary{background:#fff; color:var(--purple-5); border:2px solid var(--purple-3);}

.result-box{text-align:center; font-size:16.5px; font-weight:700; padding:14px; border-radius:14px; margin-top:16px; display:none;}
.result-good{background:#f0fdf4; color:#15803d; display:block;}
.result-mid{background:#fef9c3; color:#854d0e; display:block;}
.result-low{background:#fff1f2; color:#be123c; display:block;}

.history-box{background:#fff; border:2px solid var(--purple-2); border-radius:16px; padding:14px 18px; margin-top:14px; display:none;}
.history-box.show{display:block;}
.history-box .title{font-weight:700; color:var(--purple-5); margin-bottom:8px; font-size:14px;}
.history-row{display:flex; justify-content:space-between; font-size:12.5px; color:#6d28d9; padding:5px 0; border-bottom:1px dashed var(--purple-2);}
.history-row:last-child{border-bottom:none;}

.footer-note{text-align:center; color:#a855f7; font-size:12.5px; margin-top:28px; opacity:0.85;}
</style>
</head>
<body>

<div class="floaty f1">⭐</div>
<div class="floaty f2">🎀</div>
<div class="floaty f3">🧸</div>
<div class="floaty f4">🌈</div>
<div class="floaty f5">✨</div>
<div class="floaty f6">📐</div>
<div class="floaty f7">🎵</div>

<div class="wrap">
  <header>
    <h1>🌸 Ôn Tập Từ Vựng: Hình Dạng & Cảm Giác 🌸</h1>
    <p>19 từ mới — hình dạng, ký hiệu và cảm giác khi chạm</p>
  </header>

  <div class="theory-box">
    <span class="title">📌 Bài ôn tập này giúp em nhớ từ lâu hơn nhờ:</span>
    • <b>Hình ảnh hoá (dual coding):</b> Các từ chỉ hình dạng có hình minh hoạ đi kèm — não bộ ghi nhớ tốt hơn khi vừa có chữ vừa có hình.<br>
    • <b>Phân nhóm (chunking):</b> 19 từ được chia thành 2 nhóm nhỏ dễ nhớ thay vì học một danh sách dài.<br>
    • <b>Hồi tưởng chủ động (active recall):</b> Phần luyện tập không cho sẵn đáp án — em phải tự nhớ lại trước khi xem gợi ý.<br>
    • <b>Xen kẽ (interleaving):</b> Câu luyện tập trộn lẫn cả 2 nhóm từ, giúp phân biệt và nhớ sâu hơn.
  </div>

  <div class="tabs">
    <button class="tab-btn active" onclick="showTab('vocab')">📖 Từ vựng</button>
    <button class="tab-btn" onclick="showTab('category')">🧩 Phân loại</button>
    <button class="tab-btn" onclick="showTab('practice')">✍️ Điền từ</button>
  </div>

  <!-- ============ VOCAB TAB ============ -->
  <div id="vocab" class="panel active">
    <div class="section-title">Nhóm 1 — Hình dạng & Ký hiệu 🔷</div>
    <div class="section-sub">Các từ dùng để miêu tả hình dạng và biểu tượng</div>

    <div class="card">
      <div class="icon-box">🗣️</div>
      <div class="card-body">
        <div class="word-row"><span class="word">describe</span><span class="ipa">/dɪˈskraɪb/</span><span class="pos">v</span></div>
        <div class="meaning">miêu tả</div>
        <div class="mnemonic">💡 Mẹo: "de-<b>SCRIBE</b>" nghe giống "scribe" (người ghi chép) — ghi chép lại để miêu tả điều gì đó.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box"><svg viewBox="0 0 40 40"><circle cx="20" cy="20" r="16" fill="none" stroke="#8b5cf6" stroke-width="4"/></svg></div>
      <div class="card-body">
        <div class="word-row"><span class="word">circle</span><span class="ipa">/ˈsɜːrkl/</span><span class="pos">n</span></div>
        <div class="meaning">hình tròn</div>
        <div class="mnemonic">💡 Mẹo: liên tưởng "circus" (rạp xiếc) — nơi có vòng tròn biểu diễn.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">💿</div>
      <div class="card-body">
        <div class="word-row"><span class="word">Compact disc</span><span class="ipa">/ˌkɑːmpækt ˈdɪsk/</span><span class="pos">n</span></div>
        <div class="meaning">đĩa nghe nhạc (CD)</div>
        <div class="mnemonic">💡 Mẹo: em đã quen chữ viết tắt "<b>CD</b>" rồi — "compact" nghĩa là nhỏ gọn.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">⚖️</div>
      <div class="card-body">
        <div class="word-row"><span class="word">equal</span><span class="ipa">/ˈiːkwəl/</span><span class="pos">a</span></div>
        <div class="meaning">bằng nhau</div>
        <div class="mnemonic">💡 Mẹo: liên tưởng dấu "=" (equal sign) trong Toán học mà em đã quen thuộc.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box"><svg viewBox="0 0 40 40"><rect x="5" y="10" width="30" height="20" fill="none" stroke="#8b5cf6" stroke-width="4"/></svg></div>
      <div class="card-body">
        <div class="word-row"><span class="word">rectangle</span><span class="ipa">/ˈrektæŋɡl/</span><span class="pos">n</span></div>
        <div class="meaning">hình chữ nhật</div>
        <div class="mnemonic">💡 Mẹo: "rect-" (thẳng, vuông) + "<b>angle</b>" (góc) — em đã biết "angle" trong "triangle".</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🪞</div>
      <div class="card-body">
        <div class="word-row"><span class="word">similar</span><span class="ipa">/ˈsɪmələr/</span><span class="pos">a</span></div>
        <div class="meaning">giống nhau</div>
        <div class="mnemonic">💡 Mẹo: gần giống "simulation" (mô phỏng) — mô phỏng nghĩa là làm cho <b>giống</b> với cái thật.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box"><svg viewBox="0 0 40 40"><polygon points="20,7 34,33 6,33" fill="none" stroke="#8b5cf6" stroke-width="4"/></svg></div>
      <div class="card-body">
        <div class="word-row"><span class="word">triangle</span><span class="ipa">/ˈtraɪæŋɡl/</span><span class="pos">n</span></div>
        <div class="meaning">hình tam giác</div>
        <div class="mnemonic">💡 Mẹo: "<b>tri-</b>" = ba (như "tricycle" - xe đạp 3 bánh) + "angle" (góc) → 3 góc.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🎻</div>
      <div class="card-body">
        <div class="word-row"><span class="word">orchestra</span><span class="ipa">/ˈɔːrkɪstrə/</span><span class="pos">n</span></div>
        <div class="meaning">ban nhạc, dàn nhạc (giao hưởng)</div>
        <div class="mnemonic">💡 Mẹo: từ mượn quen thuộc "dàn nhạc <b>orchestra</b>" hay xuất hiện trong phim hoạt hình.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🔤</div>
      <div class="card-body">
        <div class="word-row"><span class="word">stand for</span><span class="ipa"></span><span class="pos">phrase v</span></div>
        <div class="meaning">viết tắt cho, đại diện cho</div>
        <div class="mnemonic">💡 Mẹo: nghĩa đen là "đứng thay cho" — chữ viết tắt "đứng thay" cho cả cụm từ dài.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🎗️</div>
      <div class="card-body">
        <div class="word-row"><span class="word">represent</span><span class="ipa">/ˌreprɪˈzent/</span><span class="pos">v</span></div>
        <div class="meaning">đại diện</div>
        <div class="mnemonic">💡 Mẹo: "re-" + "<b>present</b>" (hiện diện) → hiện diện thay mặt cho ai đó.</div>
      </div>
    </div>

    <div class="section-title" style="margin-top:22px;">Nhóm 2 — Cảm giác khi chạm 🖐️</div>
    <div class="section-sub">Các từ miêu tả bề mặt và cảm giác khi sờ vào</div>

    <div class="card">
      <div class="icon-box">🛹</div>
      <div class="card-body">
        <div class="word-row"><span class="word">flat</span><span class="ipa">/flæt/</span><span class="pos">a</span></div>
        <div class="meaning">bằng phẳng</div>
        <div class="mnemonic">💡 Mẹo: liên tưởng "flat tire" (lốp xe bị xẹp) mà em đã quen thuộc.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🧴</div>
      <div class="card-body">
        <div class="word-row"><span class="word">smooth</span><span class="ipa">/smuːð/</span><span class="pos">a</span></div>
        <div class="meaning">trôi chảy, mềm mại</div>
        <div class="mnemonic">💡 Mẹo: đọc "smooth" như bàn tay lướt êm — mượt mà, mềm mại.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🤕</div>
      <div class="card-body">
        <div class="word-row"><span class="word">bump</span><span class="ipa">/bʌmp/</span><span class="pos">n</span></div>
        <div class="meaning">chỗ bị sưng lên, sự va mạnh</div>
        <div class="mnemonic">💡 Mẹo: âm thanh "bụp!" giống tiếng va chạm mạnh.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🍬</div>
      <div class="card-body">
        <div class="word-row"><span class="word">lump</span><span class="ipa">/lʌmp/</span><span class="pos">n</span></div>
        <div class="meaning">chỗ sưng lên (cục u)</div>
        <div class="mnemonic">💡 Mẹo: gần giống "bump" nhưng là cục tĩnh — như "a lump of sugar" (một cục đường).</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🧣</div>
      <div class="card-body">
        <div class="word-row"><span class="word">silk</span><span class="ipa">/sɪlk/</span><span class="pos">n</span></div>
        <div class="meaning">lụa</div>
        <div class="mnemonic">💡 Mẹo: từ vay mượn quen thuộc "áo lụa <b>silk</b>" mềm mịn.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🪨</div>
      <div class="card-body">
        <div class="word-row"><span class="word">rough</span><span class="ipa">/rʌf/</span><span class="pos">a</span></div>
        <div class="meaning">thô ráp, xù xì</div>
        <div class="mnemonic">💡 Mẹo: đọc gần giống "rấp" — xù xì, trái nghĩa với "smooth".</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🧻</div>
      <div class="card-body">
        <div class="word-row"><span class="word">sandpaper</span><span class="ipa">/ˈsændpeɪpər/</span><span class="pos">n</span></div>
        <div class="meaning">giấy nhám</div>
        <div class="mnemonic">💡 Mẹo: "sand" (cát) + "paper" (giấy) — em đã biết cả hai từ này rồi.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">😐</div>
      <div class="card-body">
        <div class="word-row"><span class="word">dull</span><span class="ipa">/dʌl/</span><span class="pos">a</span></div>
        <div class="meaning">buồn tẻ / cùn</div>
        <div class="mnemonic">💡 Mẹo: dao cùn ("dull knife") thì không cắt được gì, cũng như một buổi học "dull" thì chán.</div>
      </div>
    </div>

    <div class="card">
      <div class="icon-box">🔪</div>
      <div class="card-body">
        <div class="word-row"><span class="word">blade</span><span class="ipa">/bleɪd/</span><span class="pos">n</span></div>
        <div class="meaning">lưỡi dao</div>
        <div class="mnemonic">💡 Mẹo: liên tưởng "razor blade" (lưỡi dao cạo) hoặc giày trượt "roller blade".</div>
      </div>
    </div>
  </div>

  <!-- ============ CATEGORY TAB ============ -->
  <div id="category" class="panel">
    <div class="section-title">🧩 Phân loại từ vựng</div>
    <div class="section-sub">Chọn đúng nhóm cho mỗi từ (giúp não bộ sắp xếp và ghi nhớ tốt hơn)</div>

    <div class="cat-grid" id="catGrid">
      <!-- filled by JS -->
    </div>

    <div class="check-row">
      <button class="btn btn-primary" onclick="checkCategory()">✅ Kiểm tra phân loại</button>
      <button class="btn btn-secondary" onclick="resetCategory()">🔄 Làm lại</button>
    </div>
    <div id="result-category" class="result-box"></div>
  </div>

  <!-- ============ PRACTICE TAB ============ -->
  <div id="practice" class="panel">
    <div class="section-title">✍️ Điền từ vào câu</div>
    <div class="section-sub">Không có ngân hàng từ — cố nhớ trước khi bấm gợi ý nhé!</div>

    <div class="sentence-card"><span class="num">1.</span>Can you <input class="blank-input" id="p1" data-answer="describe"> what your dream house looks like?<button class="hint-btn" onclick="hint(1,'d...')">💡</button><div class="hint-text" id="h1"></div></div>
    <div class="sentence-card"><span class="num">2.</span>The wheels of a bicycle are shaped like a <input class="blank-input" id="p2" data-answer="circle">.<button class="hint-btn" onclick="hint(2,'c...')">💡</button><div class="hint-text" id="h2"></div></div>
    <div class="sentence-card"><span class="num">3.</span>He copied the songs onto a <input class="blank-input" id="p3" data-answer="compactdisc"> before giving it to his friend.<button class="hint-btn" onclick="hint(3,'c...d...')">💡</button><div class="hint-text" id="h3"></div></div>
    <div class="sentence-card"><span class="num">4.</span>Both drawings are the same size, so their areas are <input class="blank-input" id="p4" data-answer="equal">.<button class="hint-btn" onclick="hint(4,'e...')">💡</button><div class="hint-text" id="h4"></div></div>
    <div class="sentence-card"><span class="num">5.</span>A door is usually shaped like a <input class="blank-input" id="p5" data-answer="rectangle">, with four right angles.<button class="hint-btn" onclick="hint(5,'r...')">💡</button><div class="hint-text" id="h5"></div></div>
    <div class="sentence-card"><span class="num">6.</span>Her handwriting is very <input class="blank-input" id="p6" data-answer="similar"> to her sister's — it's hard to tell them apart.<button class="hint-btn" onclick="hint(6,'s...')">💡</button><div class="hint-text" id="h6"></div></div>
    <div class="sentence-card"><span class="num">7.</span>A slice of pizza often looks like a <input class="blank-input" id="p7" data-answer="triangle">.<button class="hint-btn" onclick="hint(7,'t...')">💡</button><div class="hint-text" id="h7"></div></div>
    <div class="sentence-card"><span class="num">8.</span>The school <input class="blank-input" id="p8" data-answer="orchestra"> played beautiful music at the concert.<button class="hint-btn" onclick="hint(8,'o...')">💡</button><div class="hint-text" id="h8"></div></div>
    <div class="sentence-card"><span class="num">9.</span>In text messages, "LOL" <input class="blank-input" id="p9" data-answer="standsfor"> "laugh out loud."<button class="hint-btn" onclick="hint(9,'s... f...')">💡</button><div class="hint-text" id="h9"></div></div>
    <div class="sentence-card"><span class="num">10.</span>This new flag will <input class="blank-input" id="p10" data-answer="represent"> our whole school in the competition.<button class="hint-btn" onclick="hint(10,'r...')">💡</button><div class="hint-text" id="h10"></div></div>
    <div class="sentence-card"><span class="num">11.</span>After ironing, the shirt felt completely <input class="blank-input" id="p11" data-answer="flat">, with no wrinkles at all.<button class="hint-btn" onclick="hint(11,'f...')">💡</button><div class="hint-text" id="h11"></div></div>
    <div class="sentence-card"><span class="num">12.</span>Baby lotion makes your skin feel very <input class="blank-input" id="p12" data-answer="smooth">.<button class="hint-btn" onclick="hint(12,'s...')">💡</button><div class="hint-text" id="h12"></div></div>
    <div class="sentence-card"><span class="num">13.</span>He got a big <input class="blank-input" id="p13" data-answer="bump"> on his head after falling off his bike.<button class="hint-btn" onclick="hint(13,'b...')">💡</button><div class="hint-text" id="h13"></div></div>
    <div class="sentence-card"><span class="num">14.</span>There was a <input class="blank-input" id="p14" data-answer="lump"> in the mattress that made it uncomfortable to sleep on.<button class="hint-btn" onclick="hint(14,'l...')">💡</button><div class="hint-text" id="h14"></div></div>
    <div class="sentence-card"><span class="num">15.</span>The scarf is made of <input class="blank-input" id="p15" data-answer="silk">, so it feels soft and shiny.<button class="hint-btn" onclick="hint(15,'s...')">💡</button><div class="hint-text" id="h15"></div></div>
    <div class="sentence-card"><span class="num">16.</span>The tree bark felt very <input class="blank-input" id="p16" data-answer="rough"> under my fingers.<button class="hint-btn" onclick="hint(16,'r...')">💡</button><div class="hint-text" id="h16"></div></div>
    <div class="sentence-card"><span class="num">17.</span>We used <input class="blank-input" id="p17" data-answer="sandpaper"> to smooth down the rough edges of the wood.<button class="hint-btn" onclick="hint(17,'s...')">💡</button><div class="hint-text" id="h17"></div></div>
    <div class="sentence-card"><span class="num">18.</span>The knife was too <input class="blank-input" id="p18" data-answer="dull"> to cut through the bread properly.<button class="hint-btn" onclick="hint(18,'d...')">💡</button><div class="hint-text" id="h18"></div></div>
    <div class="sentence-card"><span class="num">19.</span>Be careful — the <input class="blank-input" id="p19" data-answer="blade"> of that knife is extremely sharp.<button class="hint-btn" onclick="hint(19,'b...')">💡</button><div class="hint-text" id="h19"></div></div>

    <div class="check-row">
      <button class="btn btn-primary" onclick="checkPractice()">📤 Nộp bài</button>
      <button class="btn btn-secondary" onclick="resetPractice()">🔄 Làm lại</button>
    </div>
    <div id="result-practice" class="result-box"></div>
    <div id="historyBox" class="history-box">
      <div class="title">📅 Lịch sử ôn tập (quay lại sau 1-2 ngày để nhớ lâu hơn nhé!)</div>
      <div id="historyList"></div>
    </div>
  </div>

  <div class="footer-note">💜 Học hình ảnh + chữ + luyện tập chủ động = nhớ lâu hơn rất nhiều! 💜</div>
</div>

<script>
function showTab(id){
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  const idx = ['vocab','category','practice'].indexOf(id);
  document.querySelectorAll('.tab-btn')[idx].classList.add('active');
}

const catWords = [
  {w:'describe', cat:'shape'}, {w:'circle', cat:'shape'}, {w:'Compact disc', cat:'shape'},
  {w:'equal', cat:'shape'}, {w:'rectangle', cat:'shape'}, {w:'similar', cat:'shape'},
  {w:'triangle', cat:'shape'}, {w:'orchestra', cat:'shape'}, {w:'stand for', cat:'shape'},
  {w:'represent', cat:'shape'},
  {w:'flat', cat:'touch'}, {w:'smooth', cat:'touch'}, {w:'bump', cat:'touch'},
  {w:'lump', cat:'touch'}, {w:'silk', cat:'touch'}, {w:'rough', cat:'touch'},
  {w:'sandpaper', cat:'touch'}, {w:'dull', cat:'touch'}, {w:'blade', cat:'touch'}
];

// shuffle for interleaving
function shuffle(arr){
  const a = arr.slice();
  for(let i=a.length-1;i>0;i--){
    const j = Math.floor(Math.random()*(i+1));
    [a[i],a[j]]=[a[j],a[i]];
  }
  return a;
}

const shuffled = shuffle(catWords);
const catGrid = document.getElementById('catGrid');
shuffled.forEach((item, idx)=>{
  const div = document.createElement('div');
  div.className = 'cat-item';
  div.setAttribute('data-correct', item.cat);
  div.innerHTML = `<span>${item.w}</span>
    <select id="cat${idx}">
      <option value="">-- chọn --</option>
      <option value="shape">🔷 Hình dạng</option>
      <option value="touch">🖐️ Cảm giác</option>
    </select>`;
  catGrid.appendChild(div);
});

function checkCategory(){
  const items = document.querySelectorAll('.cat-item');
  let correct = 0;
  items.forEach(item=>{
    const sel = item.querySelector('select');
    const correctVal = item.getAttribute('data-correct');
    item.classList.remove('correct','wrong');
    if(sel.value === correctVal){ item.classList.add('correct'); correct++; }
    else if(sel.value !== ''){ item.classList.add('wrong'); }
  });
  showResult('result-category', correct, items.length);
}

function resetCategory(){
  document.querySelectorAll('.cat-item select').forEach(s=>s.value='');
  document.querySelectorAll('.cat-item').forEach(i=>i.classList.remove('correct','wrong'));
  document.getElementById('result-category').classList.remove('result-good','result-mid','result-low');
  document.getElementById('result-category').innerHTML='';
}

function hint(num, letters){
  const el = document.getElementById('h'+num);
  el.textContent = '🔤 Gợi ý: bắt đầu bằng "' + letters + '"';
  el.style.display = 'block';
}

function normalize(str){ return str.trim().toLowerCase().replace(/\s+/g,''); }

function checkPractice(){
  let correct = 0;
  const inputs = document.querySelectorAll('#practice .blank-input');
  inputs.forEach(inp=>{
    const answer = normalize(inp.getAttribute('data-answer'));
    const given = normalize(inp.value);
    inp.classList.remove('correct','wrong');
    if(given === answer){ inp.classList.add('correct'); correct++; }
    else{ inp.classList.add('wrong'); }
  });
  showResult('result-practice', correct, inputs.length, true);
}

function resetPractice(){
  document.querySelectorAll('#practice .blank-input').forEach(inp=>{
    inp.value=''; inp.classList.remove('correct','wrong');
  });
  document.querySelectorAll('#practice .hint-text').forEach(h=>{ h.style.display='none'; h.textContent=''; });
  document.getElementById('result-practice').classList.remove('result-good','result-mid','result-low');
  document.getElementById('result-practice').innerHTML='';
}

function showResult(boxId, correct, total, saveHistory){
  const box = document.getElementById(boxId);
  box.classList.remove('result-good','result-mid','result-low');
  const ratio = correct/total;
  let cls, msg, emoji;
  if(ratio === 1){ cls='result-good'; emoji='🎉🌟'; msg='Xuất sắc! Em nhớ hết rồi!'; }
  else if(ratio >= 0.7){ cls='result-mid'; emoji='👏😊'; msg='Khá tốt! Xem lại vài từ sai rồi thử lại nhé!'; }
  else{ cls='result-low'; emoji='💪📖'; msg='Chưa sao, quay lại phần Từ vựng ôn thêm rồi thử lại nha!'; }
  box.classList.add(cls);
  box.innerHTML = `${emoji} Đúng ${correct}/${total} — ${msg}`;

  if(saveHistory){
    try{
      let history = JSON.parse(localStorage.getItem('shape_touch_history') || '[]');
      const now = new Date();
      history.push({date: now.toLocaleDateString('vi-VN') + ' ' + now.toLocaleTimeString('vi-VN',{hour:'2-digit',minute:'2-digit'}), correct, total});
      if(history.length > 8) history = history.slice(history.length-8);
      localStorage.setItem('shape_touch_history', JSON.stringify(history));
      renderHistory();
    }catch(e){}
  }
  box.scrollIntoView({behavior:'smooth', block:'center'});
}

function renderHistory(){
  try{
    const history = JSON.parse(localStorage.getItem('shape_touch_history') || '[]');
    if(history.length === 0) return;
    const box = document.getElementById('historyBox');
    const list = document.getElementById('historyList');
    list.innerHTML = '';
    history.slice().reverse().forEach(h=>{
      const row = document.createElement('div');
      row.className = 'history-row';
      row.innerHTML = `<span>${h.date}</span><span>${h.correct}/${h.total} điểm</span>`;
      list.appendChild(row);
    });
    box.classList.add('show');
  }catch(e){}
}
renderHistory();
</script>

</body>
</html>
