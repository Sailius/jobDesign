<header>
        <div class="company_logo">
            <img
                id="company_logo"
                src="/images/PrLogo.webp"
                alt="Логотип Pr-компании"
            />
        </div>
        <nav>
            <a href="#0">О нас</a>
            <a href="#0">Услуги</a>
            <a href="#0">Города</a>
            <a href="#0">Контакты</a>
        </nav>
        <div class="leave_request">
            Оставить заявку
        </div>
</header>

<style>
    header {
        position: fixed;
        top: 10px;
        width: 95%;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 15px;
        background-color: #00000080;
        color: #eee;
        font-weight: 500;
        font-size: 20px;
        border-radius: 10px;
        padding: 0 15px;
        z-index: 999;
    }

    .company_logo {
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: left;
        padding-left: 4px;
        width: 50px;
        height: 36px;
        background-color: #eee;
        border-radius: 5px;
    }

    img#company_logo {
        height: 32px
    }

    nav {
        width: 600px;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        gap: 15px;
    }

    nav > a {
        transition: ease 0.25s;
    }

    nav > a:hover {
        transform: scale(1.1);
    }

    .leave_request {
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        /* background-color: #cd062480; cdffcf fff*/
        background-color: #ffebcd;
        color: #010101;
        border-radius: 5px;
        font-size: 16px;
        width: 200px;
        height: 36px;
        transition: ease 0.5s;
    }

    .leave_request:hover {
        background-color: #cdffcf;
    }
</style>