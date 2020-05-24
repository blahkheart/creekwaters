<template>
    <v-card>
        <v-toolbar dark flat>
            <v-toolbar-title>
                <span class="">creek</span>
                <span class="font-weight-bold purple--text">Waters</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

        </v-toolbar>
        <v-navigation-drawer v-model="drawer" app class="grey lighten-4" temporary>
            <v-list nav dense>
                <v-list-item-group active-class="deep-purple--text text--accent-4">
                    <v-list-item v-for="link in drawerLinks" :key="link.text" link router :to="link.route">
                        <v-list-item-icon>
                            <v-icon>{{link.icon}}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>{{link.text}}</v-list-item-title>
                    </v-list-item>
                    
                    <!-- <v-list-group prepend-icon="mdi-room-service" no-action>
                        <template v-slot:activator>
                            <v-list-item-content>
                                <v-list-item-title >Services</v-list-item-title>
                            </v-list-item-content>
                        </template>
                
                        <v-list-item
                            v-for="service in services"
                            :key="service[0]"
                        >
                            <v-list-item-title v-text="service[0]"></v-list-item-title>
                            <v-list-item-icon>
                                <v-icon>{{service[1]}}</v-icon>
                            </v-list-item-icon>
                        </v-list-item>
                    </v-list-group> -->
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </v-card>
</template>

<script>
export default {
    data:  ()=> ({
        drawer: false,
        drawerLinks: [
            {icon: 'mdi-home', text: 'Home', route: '/'},
            {icon: 'mdi-bookshelf', text: 'About', route: '/about'},
            {icon: 'perm_contact_calendar', text: 'Contact', route: '/contact'}
            // {icon: 'mdi-room-service', text: 'Services', route: '/services'}
        ],
        services: [
            ['SEO', 'settings'],
            ['Google PPC', 'mdi-account-cash'],
            ['Email Marketing', 'mdi-email-open'],
            ['Social Media MArketing', 'people_outline']
        ]
    }) 
}
</script>