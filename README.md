<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài 12 – Nhóm 4 Lớp 12 Anh</title>
<style>
body {
    font-family: Arial, sans-serif;
    background: #FFF4B7;
    margin: 0;
}
header {
    background: linear-gradient(135deg, #000B58, #003161);
    color: white;
    text-align: center;
    padding: 40px 20px;
}
h1 {margin: 0; font-size: 36px;}
h2 {color: #000B58;}
section {background: white; margin: 20px auto; width: 90%; max-width: 900px; padding: 20px; border-radius: 12px; box-shadow: 0 6px 15px rgba(0,0,0,0.15);} 
.details {display: none; margin-top: 15px;}
button {background: #006A67; color: white; padding: 10px 16px; border: none; border-radius: 8px; cursor: pointer;}
button:hover {background: #003161;}
fieldset {margin-bottom: 15px; border-radius: 8px;}

/* Thêm font đẹp */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
body { font-family: 'Poppins', sans-serif; }

/* Nền thêm họa tiết nhẹ */
body {
    background: #FFF4B7 url('https://www.transparenttextures.com/patterns/cubes.png');
}

/* Header thêm logo + đổ bóng */
header img.logo {
    width: 110px;
    filter: drop-shadow(0 4px 6px rgba(0,0,0,0.25));
    margin-bottom: 12px;
}

/* Nút mượt hơn */
button {
    transition: 0.3s;
    font-weight: 600;
}
button:hover {
    transform: scale(1.05);
}

/* Section hiệu ứng nổi */
section {
    transition: 0.3s;
}
section:hover {
    transform: translateY(-5px);
}

/* Iframe bo góc */
iframe {
    border-radius: 12px;
    border: 2px solid #003161;
}


/* MENU CHUYÊN NGHIỆP */
nav.topmenu {
    width:100%;
    background:#003161cc;
    backdrop-filter: blur(4px);
    position:fixed;
    top:0;
    left:0;
    padding:12px 25px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    z-index:100;
}
nav.topmenu a {
    color:white;
    text-decoration:none;
    font-weight:600;
    margin-right:18px;
    transition:.25s;
}
nav.topmenu a:hover {
    color:#FFD93D;
    transform: translateY(-2px);
}
</style>
<script>
function toggle(id){
  var x=document.getElementById(id);
  x.style.display = x.style.display==="block" ? "none" : "block";
}

// Hiệu ứng mở section mượt hơn
function toggle(id){
  var box=document.getElementById(id);
  if(box.style.display==="block"){
     box.style.opacity=0;
     setTimeout(()=>{ box.style.display="none"; },200);
  } else {
     box.style.display="block";
     setTimeout(()=>{ box.style.opacity=1; },10);
  }
}

// Hiệu ứng cuộn mượt + nảy (bounce)
function bounceScroll(targetID){
    const el = document.getElementById(targetID);
    if(!el) return;
    // Cuộn mượt
    el.scrollIntoView({ behavior: 'smooth', block: 'start' });

    // Sau khi cuộn xong thì nảy
    setTimeout(()=>{
        el.style.transition = 'transform 0.25s ease';
        el.style.transform = 'translateY(-10px)';
        setTimeout(()=>{
            el.style.transform = 'translateY(0)';
        }, 250);
    }, 500);
}
</script>
</head>
<body>
<nav class="topmenu">
    <div>
        <a href="file:///C:/Users/Win10/Downloads/index.html">⬅ Quay lại</a>
        <a href="javascript:bounceScroll('luyentap-section')">Luyện tập</a>
        <a href="javascript:bounceScroll('vd1-section')">Vận dụng 1</a>
        <a href="javascript:bounceScroll('vd2-section')">Vận dụng 2</a>
    </div>
</nav>
<br><br><br>
<header>
    <nav style="position:absolute; top:15px; left:20px;">
        <a href="file:///C:/Users/Win10/Downloads/index.html" style="background:#FFF4B7; padding:8px 14px; border-radius:8px; color:#000B58; text-decoration:none; font-weight:700;">⬅ QUAY LẠI</a>
    </nav>
    <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/HTML5_Badge.svg/768px-HTML5_Badge.svg.png">
    <h1 style="font-size:32px; font-weight:600;">Nhóm 4 – Lớp 12 Anh</h1>
    <h2 style="font-size:50px; font-weight:900; margin-top:12px; letter-spacing:1.5px; color:#FFD93D; text-shadow:0 4px 10px rgba(0,0,0,0.35);">BÀI 12: TẠO BIỂU MẪU</h2>
    
</header>

<!-- LUYỆN TẬP -->
<section id="luyentap-section">
    <h2>1. Luyện tập</h2>
    <button onclick="toggle('luyentap')">Hiện / Ẩn bài làm</button>
    <div id="luyentap" class="details">
        <h3>Tạo các phần tử form và liệt kê ví dụ</h3>
        <form>
            <fieldset>
                <legend>Label + Input (text)</legend>
                <label for="ten">Họ tên:</label>
                <input type="text" id="ten"> 
                <p>Ví dụ sử dụng: nhập tên, nhập địa chỉ, nhập trường học.</p>
            </fieldset>
            <fieldset>
                <legend>Input password</legend>
                <input type="password"> 
                <p>Ví dụ: mật khẩu đăng nhập, mã PIN, mật khẩu wifi.</p>
            </fieldset>
            <fieldset>
                <legend>Input radio</legend>
                <input type="radio" name="gt"> Nam
                <input type="radio" name="gt"> Nữ
                <p>Ví dụ: chọn giới tính, chọn lớp, chọn ca học.</p>
            </fieldset>
            <fieldset>
                <legend>Input checkbox</legend>
                <input type="checkbox"> Đọc sách
                <input type="checkbox"> Xem phim
                <p>Ví dụ: chọn sở thích, chọn môn học yêu thích, chọn tùy chọn thêm.</p>
            </fieldset>
            <fieldset>
                <legend>Input button</legend>
                <input type="button" value="Nhấn thử">
                <p>Ví dụ: nút chạy lệnh, nút mở hộp thoại, nút đổi màu.</p>
            </fieldset>
            <fieldset>
                <legend>Input file</legend>
                <input type="file">
                <p>Ví dụ: tải ảnh, tải video, tải tài liệu.</p>
            </fieldset>
            <fieldset>
                <legend>Input submit</legend>
                <input type="submit" value="Gửi dữ liệu">
                <p>Ví dụ: gửi biểu mẫu đăng ký, gửi khảo sát, gửi phản hồi.</p>
            </fieldset>
            <fieldset>
                <legend>Select</legend>
                <label for="lop">Chọn lớp:</label>
                <select id="lop">
                    <option value="10">10</option>
                    <option value="11">11</option>
                    <option value="12">12</option>
                </select>
                <p>Ví dụ: chọn lớp, chọn màu sắc, chọn môn học.</p>
            </fieldset>
            <fieldset>
                <legend>Textarea</legend>
                <textarea rows="4" cols="40">Nhập ghi chú...</textarea>
                <p>Ví dụ: ghi chú, mô tả sản phẩm, phản hồi.</p>
            </fieldset>
        </form>
    </div>
</section>

<!-- VẬN DỤNG 1 -->
<section id="vd1-section">
    <h2>2. Vận dụng 1</h2>
    <button onclick="toggle('vd1')">Hiện / Ẩn bài làm</button>
    <div id="vd1" class="details">
        <p>Biểu mẫu đăng ký thành viên câu lạc bộ:</p>
        <a href="https://minhtuvonguyen-collab.github.io/Tin12Bai12.VD.io/" target="_blank">Nhấn để xem trang</a>
    </div>
</section>

<!-- VẬN DỤNG 2 -->
<section id="vd2-section">
    <h2>3. Vận dụng 2</h2>
    <button onclick="toggle('vd2')">Hiện / Ẩn bài làm</button>
    <div id="vd2" class="details">
        <p>Trang web nhiệm vụ 2 bài 11 hiển thị trong iframe:</p>
        <p>Đã thêm liên kết cho cụm từ <b>Đăng kí</b>.</p>
        <iframe src="https://minhtuvonguyen-collab.github.io/Nhom4Tin12Anh.Bai11.NV2/" width="100%" height="300"></iframe>
    </div>
</section>

</body>
</html>
