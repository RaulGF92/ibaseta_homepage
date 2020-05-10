<template>
    <div class="footer-page">
        <div class="footer-page_inner">
            <div class="left">
                <div class="inner">
                    <label>Mapa Sitio</label>
                    <ul>
                        <li><a href="#album">Fotografias</a></li>
                        <li><a href="#cameras">Mis Cámaras</a></li>
                        <li><a href="#contact">Contacto</a></li>
                    </ul>
                </div>
            </div>
            <div class="right">
                <ul>
                    <li>@{{datosPersonales.nombre}} 2020</li>
                    <li>License MIT</li>
                    <li>Powered by <a href="https://raulgf92.github.io/homepage/">@raulgf92</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
import mainJson from '../../../config/main.json'

export default {
    name: 'FooterPage',
    data(){
        return {
            datosPersonales: mainJson["datos-personales"]
        }
    }
}
</script>
<style lang="scss" scoped>
    .footer-page {
        display: flex;
        align-content: center;
        &_inner {
            flex: 1;
            margin: auto 1rem;
            height: 100%;
            min-height: calc(var(--footer-page-height) - 50px);
            width: 90%;
            display: flex;
            flex-direction: row;

            .left {
                flex: 2;
                text-align: center;
                
                .inner {
                    float: left;
                    margin: auto;
                    width: 25%;
                }

                label {
                    color: var(--thirdy-color);
                }

                ul {
                    border-top: 0.5px dotted var(--thirdy-color);
                    color: white;
                    list-style-type: none;
                    margin: 10px 0;
                    padding: 10px 0;
                    li {
                        margin: 5px 0;
                        padding: 0;
                    }
                }
            }

            .right {
                flex: 1;
                border-left: 1px solid var(--thirdy-color);

                ul {
                    color: white;
                    list-style-type: none;

                    a {
                        color: var(--thirdy-color);
                    }

                    li {
                        margin: 5% 0;
                    }

                    svg {
                        font-size: x-large;
                    }
                }
            }

        }

        a {
          text-decoration: none;
          &:hover {
              text-decoration: underline;
          }
        }
    }

    @media(max-width:1000px) {
        .footer-page  { 
            max-height: unset;
            &_inner {
                flex-direction: column;

                .left .inner {
                    margin: 1rem auto;
                    width: 85%;
                    float: inherit;
                }

                .right {
                    border-left: none;
                    border-top: 1px solid var(--thirdy-color);
                }
            }
        }
    }
</style>