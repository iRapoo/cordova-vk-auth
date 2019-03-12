# Cordova-plugin-auth

2019, @Rapoo

Исправленная библиотека для авторизации и получения доступа к соц. сети ВКонтакте

**Пример использования**

    initialize: function() {
            document.addEventListener('deviceready', this.onDeviceReady.bind(this), false);
    },

    onDeviceReady: function() {
        let socialBtn = $('.social-btn');

        socialBtn.click(function () {
            SocialVk.init('1234567'); //APP ID только цифры
            SocialVk.login(['offline'], function (value) {
                console.log(value); //value - вернет JSON с token и user (информация аккаунта)
            });
        });
    },

    app.initialize();