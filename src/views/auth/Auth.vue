<template>
  <section id="loginPage" 
    :style="{backgroundImage: 'url('+require('@/assets/images/bgLogin.jpg')+')'}">
    <div class="loginContent">
      <div class="loginCard">
        <div class="decor" style="background-image: url('./assets/images/building.jpg')">
          <div class="content">
            <span class="logo">
              <img :src="require('@/assets/images/logo.svg')" alt="" />
            </span>
            <span class="dots">
              <span></span>
              <span></span>
              <span></span>
            </span>
            <span class="description">
              <p>
                Os melhores e mais completos cursos de Laravel do Brasil, cursos
                com projetos reais. Do zero ao profissional.
              </p>
            </span>
            <span class="copyright fontSmall">
              Todos os Direitos reservados - <b>Especializati</b>
            </span>
          </div>
        </div>
        <div class="login">
          <div class="content">
            <span class="logo">
              <img :src="require('@/assets/images/logoDark.svg')" alt="" />
            </span>            
            <span>
              <p>Seja muito bem vindo!</p>
            </span>
            <span class="dots">
              <span></span>
              <span></span>
              <span></span>
            </span>
            <span class="description">
              Acesse nossa plataforma e desfrute de cursos completos para sua
              especialização.
            </span>
            <form action="/dist/index.html" method="">
              <div class="groupForm">
                <i class="far fa-envelope"></i>
                <input type="email" name="email" placeholder="Email" required />
              </div>
              <div class="groupForm">
                <i class="far fa-key"></i>
                <input
                  type="password"
                  name="password"
                  placeholder="Senha"
                  required
                />
                <i class="far fa-eye buttom"></i>
              </div>
              <button 
                class="btn primary" 
                type="submit"
                @click.prevent="login">
                    Login
                </button>
            </form>
            <span>
              <p class="fontSmall">
                Esqueceu sua senha?                
                <router-link 
                    :to="{name: 'forget.password'}"
                    class="link primary">
                    Clique Aqui
                </router-link>
              </p>
            </span>
          </div>
          <span class="copyright fontSmall">
            Todos os Direitos reservados - <b>Especializati</b>
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import router from '@/router'

export default {
    name: 'Auth', 
    setup() {
        const login = () => router.push({name: 'campus.home'})

        return {
            login
        }
    }
}
</script>