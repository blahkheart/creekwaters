<template>
    <v-card>
        <v-toolbar dark flat class="px-5 cw-navigation">
            <v-toolbar-title>
                <span >creek</span>
                <span class="font-weight-bold grey--text">Waters</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            
            <v-list class="hidden-md-and-down">
                <v-list-item-group
                    class="d-flex"
                >
                    <v-list-item dark class="cw-navigation-item" v-for="link in drawerLinks" :key="link.text" link router :to="link.route">
                        <v-list-item-title class="caption font-weight-medium px-4 text-uppercase">{{link.text}}</v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
            <v-tooltip bottom>
                <template v-slot:activator="{ on }">
                    <v-btn fab x-small color="deep-purple darken-3 ml-5" dark v-on="on">
                        <v-icon>mdi-text-box-search</v-icon>
                    </v-btn>
                </template>
                <span>Free Social Media Audit</span>
            </v-tooltip>
            <v-app-bar-nav-icon class="hidden-lg-and-up" @click="drawer = true"></v-app-bar-nav-icon>
        </v-toolbar>
        <v-navigation-drawer width="280" v-model="drawer" app class="grey lighten-4" temporary>
            <v-list nav dense class="py-5 mt-5">
                <v-list-item-group active-class="green--text text--accent-4">
                    <v-list-item v-for="link in drawerLinks" :key="link.text" link router :to="link.route">
                        <v-list-item-icon>
                            <v-icon>{{link.icon}}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>{{link.text}}</v-list-item-title>
                    </v-list-item>
                    
                    <v-list-group  prepend-icon="mdi-room-service" no-action>
                        <template v-slot:activator>
                            <v-list-item-content>
                                <v-list-item-title>Services</v-list-item-title>
                            </v-list-item-content>
                        </template>
          
                        <v-list-item
                            v-for="service in services"
                            :key="service[0]"
                            active-class="deep-purple--text text--accent-4"
                        >
                            <v-list-item-title class="pl-3" v-text="service[0]"></v-list-item-title>
                            <v-list-item-icon>
                                <v-icon>{{service[1]}}</v-icon>
                            </v-list-item-icon>
                        </v-list-item>
                    </v-list-group>
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
        ],
        services: [
            ['Brand Development', 'mdi-battlenet'],
            ['SEO', 'settings'],
            ['Google PPC', 'mdi-account-cash'],
            ['Email Marketing', 'mdi-email-open'],
            ['Social Media MArketing', 'people_outline']
        ]
    }) 
}
</script>

<style lang="scss" scoped>
    .cw-navigation{
        a, a:hover {
            text-decoration: none;
        }
        .v-list.v-sheet.v-sheet--tile {
            background: transparent;
        }
        &-item{
            border-bottom: 3px solid transparent;
            &.v-item--active, &.v-list-item--active{
                background: transparent;
                border-bottom: 3px solid #fff;
            }
        }
    }
</style>