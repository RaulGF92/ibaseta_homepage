<template>
    <div class="contact-info">
        <div class="contact-info-left">
            <div class="contact-info-left_inner">
                    <div class="contact-item">
                        <i class="fas fa-phone-square"></i>
                        <span>{{phone}}</span>
                    </div>
                    <br />
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>{{email}}</span>
                    </div>
            </div>
        </div>
        <div class="contact-info-right">
            <div class="contact-info-right_inner">
                <iframe src="https://maps.google.com/maps?width=100%&height=600&hl=es&q=cand%C3%A1s+()&ie=UTF8&t=&z=14&iwloc=B&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
            </div>
        </div>
    </div>
</template>
<script>
import mainJson from '../../../config/main.json'

export default {
    name: 'ContactInfo',
    data() {
        return {
            phone: mainJson["datos-personales"].telefono,
            email: mainJson["datos-personales"].email
        }
    },
}
</script>
<style lang="scss" scoped>
    .contact-info {
        display: flex;
        flex-direction: row;
        
        &-left {
            display: flex;
            flex-direction: column;
            flex: 1;
            align-content: space-between;

            &_inner {
                margin: auto;
                width: 100%;
            }

            .contact-item {

                flex:1;
                display: flex;
                flex-direction: row;
                align-content: space-between;
                
                span {
                    color: white;
                    margin: 10px 0;
                }

                svg {
                    font-size: 2.5rem;
                    color: var(--thirdy-color) !important;
                }

                * {
                    flex: 1;
                    text-align: left;
                }
            }
        }

        &-right {
            flex: 2;
        }
    }
    iframe {
        width: 100%;
        height: 100%;
        min-height: var(--contact-info-height);
    }

    @media(max-width:1000px) {
        .contact-info {
            flex-direction: column;

            &-left {
                margin-top: 1rem;
                margin-bottom: 1rem;
            }

            &-right {
                overflow: hidden;
            }

            iframe {
                max-height: var(--contact-info-height-iframe);
            }
        }
    }
</style>