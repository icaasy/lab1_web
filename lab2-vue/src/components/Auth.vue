<template>
    <main class="auth-page">
        <div class="container auth-container">

            <section class="auth-card">
                <h1>Вход</h1>

                <form>
                    <label for="login-email">Email</label>
                    <input
                        type="email"
                        id="login-email"
                        placeholder="example@mail.ru"
                        required
                    >

                    <label for="login-password">Пароль</label>
                    <input
                        type="password"
                        id="login-password"
                        placeholder="Введите пароль"
                        required
                    >

                    <button type="submit" class="button">Войти</button>
                </form>
            </section>

            <section class="auth-card">
                <h1>Регистрация</h1>

                <form>
                    <label for="register-name">Имя</label>
                    <input
                        type="text"
                        id="register-name"
                        placeholder="Ваше имя"
                        required
                    >

                    <label for="register-email">Email</label>
                    <input
                        type="email"
                        id="register-email"
                        placeholder="example@mail.ru"
                        required
                    >

                    <label for="register-password">Пароль</label>
                    <input
                        type="password"
                        id="register-password"
                        placeholder="Придумайте пароль"
                        required
                    >

                    <button type="submit" class="button">
                        Зарегистрироваться
                    </button>
                </form>
            </section>

        </div>
    </main>
</template>