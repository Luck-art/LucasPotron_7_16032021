<template>
          <header>
            <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
                <div class="container-fluid">
                  <router-link class="navbar-brand" to="/"><img src="../assets/groupomania.png"></router-link>
                  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                  </button>
                  <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                      <li class="nav-item">
                        <router-link class="nav-link" aria-current="page" to="/">Accueil</router-link>
                      </li>
                      <p>{{ $store.state.userId }}</p>
                      <div class="d-flex" v-if="$store.state.userId === 0">
                        <li class="nav-item">
                          <router-link class="nav-link" to="/register">S'enregistrer</router-link>
                        </li>
                        <li class="nav-item">
                          <router-link class="nav-link" to ="/identify">S'identifier</router-link>
                        </li>
                      </div>
                        <li v-else class="nav-item">
                          <router-link class="nav-link" to ="/myaccount">Mon compte</router-link>
                        </li>
                        <li class="nav-item">
                          <router-link class="nav-link" to="/forum">Forum</router-link>
                        </li>
                    </ul>
                  </div>
                </div>
              </nav>
            </header>            
</template>

<script>
export default {
    name: 'Header'
}
</script>
