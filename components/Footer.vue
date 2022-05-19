<template>
    <footer>
      <div class="footer__content">
        <div class="footer__background">
          <div class="footer__columns">
            <div class="footer__columns_left">
              <div class="columns_left-title">Связь с нами</div>
              <div class="columns_left-info">У вас остались вопросы? Напишите нам - мы ответим в ближайшее время!</div>
              <div class="columns_left-aside">
                <div class="phone-link">
                  <span><img src="@/static/Vector.png" alt=""> 8 (111) 222-33-44</span>
                </div>
                <div class="mail-link">
                  <span><img src="@/static/Vector4.png" alt=""> order@buhone.ru</span>
                </div>
              </div>
            </div>
            <div class="footer__columns_right">
              <div class="columns_right_regestration">
                <div class="regestration-name">
                  <span>Имя</span>
                  <input type="name">
                </div>
                <div class="regestration-subname">
                  <span>Фамилия</span>
                  <input type="name">
                </div>
                <div class="regestration-message">
                  <span>Сообщение</span>
                  <input type="text">
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style>

</style>