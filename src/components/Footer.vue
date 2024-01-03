<template>
          <footer class="footer">
            <div class="container-footer">
                <div class="footer-box">
                    <h6>Kinn Home</h6>
                    <div class="footer-line">
                        <img src="../assets/images/line.png" alt="line">
                    </div>
                    <p>Need to get in touch? Just email us at hello@kinnhome.com</p>
                </div>
                <div class="footer-nav_1">
                     <ul>
                            <li>Магазин</li>
                            <li>Стиль</li>
                            <li>О нас</li>
                            <li>Истории</li>
                     </ul>
                </div>
                 <div class="footer-nav_2">
                        <ul>
                            <li>Помощь</li>
                            <li>Контакты</li>
                            <li>Документы</li>
                            <li>FAQ</li>
                        </ul>
                 </div>
                 <div class="footer-social">
                        <img src="../assets/images/icon/social-media.png" alt="social-media">
                 </div>
            </div>
        </footer>
</template>

<script>
export default {

}
</script>

<style>
footer {

display: flex;

align-items: center;
justify-content: space-between;



height: 382px;

width: 100%;
height: 100%;
max-width: 1420px;
margin: 15px auto;

padding: 15px 15px 15px 15px;


}

.container-footer {
display: flex;
flex-wrap: wrap;
align-items: center;
align-content: space-around;
justify-content: space-around;

margin: 15px auto;
padding: 15px;
flex-shrink: 0;
background: #717353;
height: 382px;
width: 1420px;
flex-wrap: wrap;
align-items: center;
justify-content: space-between;

}

.footer-box {
color: #FFFFEF;
font-weight: 400px;
line-height: 25px;
font-size: 16px;

flex-shrink: 0;
margin: 0;
padding: 0;
}

.footer-box h6 {
height: 10px;

}

.footer-box p {
color: #FFFFEF;
font-size: 12px;
font-style: normal;
font-weight: 256px;
line-height: 25px;
}

.footer-line {
width: 40px;
height: 1px;
flex-shrink: 0;
margin-top: -20px;
}

.footer-line img {
width: 100%;
}



.footer-nav_1 li {
color: #FFFFEF;
font-family: Roboto;
font-size: 12px;
font-style: normal;
font-weight: 400;
line-height: 25.2px;
letter-spacing: 1.575px;
text-transform: uppercase;
list-style-type: none;
}



.footer-nav_2 li {
color: #FFFFEF;
font-family: Roboto;
font-size: 12px;
font-style: normal;
font-weight: 400;
line-height: 25.2px;
letter-spacing: 1.575px;
text-transform: uppercase;
list-style-type: none;
}

.footer-social {
width: 120px;
height: 22px;
flex-shrink: 0;

}

.footer-social img {
width: 100%;
}
</style>