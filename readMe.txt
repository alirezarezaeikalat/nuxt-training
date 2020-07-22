1. to create nuxt app first you need to install create-nuxt-app:

        npm install -g create-nuxt-app

2. then you can use it to make a new app: 

        create-nuxt-app <name of the project>

3. after creating the app the cli ask for several components, you can 
    select your server framework, you can your ui framework, and you can choose 
    to have server side rendering or not, you can also choose to install axios


4. you can run the development server: 

        cd <project folder>
        npm run dev

5. or you can do this for production:

        npm run build
        npm run startn

6. every .vue file in the page folder is interpreted as a route,        

7. creating the route with dynamic parameter:

        you have to create file with _ for example: 
                _id.vue
        or you can make new folder and call it _id and put index.vue in it

        and you can access it in the _id component just like this:
                {{$route.params.id}}

8. if we use normal anchor tag for routing, we load new page, and the app 
        is not single page anymore.

9. in vue app to prevent this behavior we use 
        <router-link to=""></router-link>

10. in nuxt we use <nuxt-link to=""></nuxt-link>

11. we can also use javascript for routing:
        (this is the normal vue behavior)

        methods: {
                onLoadUser() {
                        this.$router.push('/users')
                }
        }

12. nuxt gives us validate property for validating the route param in the 
        components in the pages folder:

        validate(data) {
                console.log(data)
                return ;
        }

13. we can use certain element in all of the childs in the specific
        folder, you have to create a .vue file with name same as
        the folder name and add the code you want in it and add 
        <nuxt-child /> in it

14. The name for the the layout component is default.vue and 
        in the template it has the <nuxt /> component in it

15. you can add new layout and use it only in certain pages:

        a. first you have to make the new component in layout
                folder

        b. then you have to add layout properties in the 
        components that you want to use new layout.

                layout: 'user'

16. if you add error.vue to the layout folder, you can make 
        customized error page

17. we can make global css files, we can make styles folder in 
        the assets folder, and make .css file in it, and 
        then add this in the css section of nuxt.config.js file:

        css: [
                '~/assets/styles/main.css'
        ],

18. If you want to add anything to the head section of the html,
        you can add it to the nuxt.config.js file.