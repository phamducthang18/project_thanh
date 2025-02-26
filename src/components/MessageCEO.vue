<template>
    <div class="main-inner">
        <div class="ceo-message">
            <h2>Message from the CEO</h2>
            <p>On behalf of the Board of Directors and all employees of Long Wall, I would like to extend my deepest gratitude for the trust and support of our valued customers and partners.</p>

            <h3>"Expanding Our Horizons with Offshore Development"</h3>
            <p>We are committed to delivering high-quality services tailored to the global market.</p>
            
            <ul>
                <li>Because we want to <strong>create more job opportunities</strong> for young Vietnamese talents through cutting-edge technology.</li>
                <li>Because we aim to <strong>learn from the expertise and business experience</strong> of international markets.</li>
                <li>Because we aspire to <strong>bring world-class services and solutions</strong> to Vietnam in the future.</li>
            </ul>

            <p><strong>Director</strong><br>
            Long Wall Technology Corporation<br>
            </p>
        </div>

        <div class="people-first">
            <h2>"People First" - Developing Talents for the Future</h2>
            <p>I firmly believe that <strong>"Employees are the core strength of an enterprise"</strong>, much like the famous saying, <em>"Talent is the nation's treasure."</em></p>

            <p>Vietnam has a vast pool of IT engineers, yet there is still a gap in experience and expertise.</p>

            <p>To deliver high-quality services and exceed customer expectations, companies need:</p>
            
            <ul>
                <li>Leaders and employees who are <strong>self-driven learners, continuously improving</strong> their knowledge and skills.</li>
                <li>A work environment that <strong>encourages professional growth and innovation</strong>.</li>
            </ul>

            <p>At Long Wall, we foster a culture of learning, ensuring that every individual is empowered with the necessary skills to thrive. We provide continuous training and, when needed, collaborate with industry experts to enhance our workforce.</p>

            <h3>Three Key Factors in Employee Development:</h3>
            <ul>
                <li><strong>Mindset and Critical Thinking</strong> – Cultivating a proactive and problem-solving approach.</li>
                <li><strong>Language Proficiency</strong> – English and other relevant languages to excel in the global market.</li>
                <li><strong>Technology & Quality Management</strong> – Mastering cutting-edge technology and maintaining high-quality standards.</li>
            </ul>

            <p>We are dedicated to nurturing the next generation of professionals, ensuring they are equipped to lead in a rapidly evolving technological landscape.</p>
        </div>
    </div>
</template>

<style scoped>
/* Căn chỉnh bố cục chính */
.main-inner {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
}


.ceo-message, .people-first {
    width: 100%;
    max-width: 850px;
    margin-bottom: 40px;
    padding: 20px;
    /* background: #f9f9f9; */
    border-radius: 8px;
    /* box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); */
}

.ceo-message strong{
    margin-left: 5px;
    margin-right: 5px;
}
h2 {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 15px;
    position: relative;
}

h2::after {
    content: "";
    display: block;
    width: 80px;
    height: 3px;
    background-color: #E94560;
    margin: 8px auto 0;
}


.main-inner ul {
    list-style: none; 
    padding: 0;
    text-align: left; 
}

.main-inner ul li {
    display: flex;
    align-items: center;
    font-size: 16px;
    margin-bottom: 10px;
}

/* Icon check trước mỗi danh sách */
.main-inner ul li::before {
    content: "✔";
    color: #E94560;
    font-weight: bold;
    margin-right: 10px;
    font-size: 18px;
}

/* Tăng khoảng cách giữa các đoạn văn */
p {
    font-size: 16px;
    line-height: 1.6;
    margin-bottom: 15px;
}
</style>
