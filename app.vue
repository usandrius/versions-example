<template>
  <div>
    <NuxtRouteAnnouncer />
    
    <div>
      <header>
        <nav>
          <NuxtLink to="/">Главная</NuxtLink> | 
          <NuxtLink to="/about">О нас</NuxtLink>
        </nav>
      </header>
      
      <hr />
      
      <NuxtPage />
    </div>
  </div>
</template>
