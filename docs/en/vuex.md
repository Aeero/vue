# Vuex

[What is Vuex?](https://vuex.vuejs.org/)

Vuex: state management pattern + library

![alt events up](https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578371882429_1.png?alt=media&token=2c411c9f-d5cf-4404-8009-00b73e24a622 "There’s the default way of communicating events up and passing props down to share data, but that can become overly complicated.")

Vuex: single source of truth

![alt Vuex](https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578371889694_2.png?alt=media&token=f9cc01f0-4644-4867-92ad-17ccd6cc7a6e "global State")

Vuex Store: similar to the vue instance

![alt Pattern](https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578371892222_3.png?alt=media&token=911a39ae-99b2-4026-9132-71fae035ffc5 "A State Management Pattern")

mutations: commit + track state changes

> `actions` call `mutaions` update `state`

## Vuex in Motion

![alt Motion](https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578371900954_6.gif?alt=media&token=a92f02df-8800-4f4a-ac63-6690f9453e66 "Vuex in Motion")

## mutations

Mutations can update/mutate Vuex State

store.js

```js
 state: {
      count: 0
    }

mutations: {
      INCREMENT_COUNT(state) {
        state.count += 1
      }
    }
```

component

click on it to trigger this Mutation

```html
 <button @click="incrementCount">Increment</button>
```

```js

incrementCount() {
      this.$store.commit('INCREMENT_COUNT')
    },
```

![alt mutations](https://i.imgur.com/hE9cB9L.png)

## actions

![alt actions](https://i.imgur.com/eSE8uHo.png)

## Actions and Mutations

Mutations are `synchronous`
synchronous A,B,C,D,E

Actions are `asynchronous`
asynchronous A,C,E,D,B

Actions can wrap business logic around mutations

![alt metaphor](https://i.imgur.com/Io9SxCe.png)

metaphor: `ask(Actions)` sb. to `do(Mutations)` sth  

Actions don't always commit their mutations  
Always put Mutations within Actions
