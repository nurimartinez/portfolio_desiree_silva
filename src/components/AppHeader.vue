<template>
  <header>
    <nav class="header_portfolio">
      <img
        class="logo_header"
        src="../assets/icons/logo_gimp.webp"
        alt="logotipo de Desirée Silva"
      />
      <ul id="main-menu" class="main-menu">
        <li class="main-menu_item">
          <a href="#sobremi" class="main-menu_link">Sobre mí</a>
        </li>
        <li class="main-menu_item">
          <a href="#proyectos" class="main-menu_link">Proyectos</a>
        </li>
        <li class="main-menu_item">
          <a href="#formacion" class="main-menu_link">Formación</a>
        </li>
        <li class="main-menu_item">
          <a
            href="https://drive.google.com/file/d/1BUolDxQYZECSIflSKSMSiepAN9UMRVkw/view?usp=sharing"
            class="main-menu_link"
            target="_blank"
            >Ver Currículum Vitae</a
          >
        </li>
      </ul>
      <button class="button_header">
        <svg-icon type="mdi" :path="mdiPhone" class="icon_header"></svg-icon
        ><a href="tel:675937952">¡Contáctame!</a>
      </button>
    </nav>
  </header>
  <hr class="hr_portfolio" />
</template>

<script setup>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiPhone } from "@mdi/js";
</script>

<style lang="scss">
.logo_header {
  width: 15rem;
  height: fit-content;
}
.header_portfolio {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 10rem;
  align-items: center;
  justify-content: space-between;

  .main-menu {
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    text-decoration: none;
    cursor: pointer;

    &_item {
      padding: 2em;
      font-size: 1rem;
      font-weight: 500;
      cursor: pointer;
      border: none;
    }

    &_link {
      text-decoration: none;
      color: #000000;
      position: relative;
      color: inherit;
    }

    &_link::before {
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 2px;
      background: linear-gradient(to right, #ce93d8, #e878a2, #eb85ab);
      z-index: 1;
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.5s ease-in-out;
    }

    &_link:hover::before {
      transform: scaleX(1);
    }
  }

  .button_header {
    background-color: #ce93d8;
    width: 18em;
    height: fit-content;
    font-size: 1.3rem;
    font-family: "Poppins";
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
    border-radius: 0.5rem;
    border-style: none;
    cursor: pointer;
    text-decoration: none;
    text-align: center;
    justify-content: center;
    display: flex;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: all 0.3s ease;
  }

  .button_header a {
    text-decoration: none;
    color: #000000;
  }

  .icon_header {
    display: flex;
    flex-direction: row;
    align-self: center;
    width: auto;
    height: auto;
  }

  .button_header:hover {
    background-color: #ce93d8;
    transform: scale(0.95);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }
}
</style>
