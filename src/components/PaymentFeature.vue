<template>
    <div class="row">
        <div v-for="item in items" :key="item.id" class="col-lg-6 col-md-12 mb-25 wow move-up">
            <div class="ht-service-box--three">
                <div class="service-box-wrap">
                    <div class="image__media">
                        <img :src="item.icon" class="img-fluid" alt="Icon">
                    </div>
                    <div class="content">
                        <h5 class="heading font-weight--light">{{ item.heading }}</h5>
                        <div class="service_text">{{ item.text }}</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'PaymentFeature',
        data (){
            return {
                items: [
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-01.png'),
                         heading:'ТСЖ, ЖСК и ЖЭУ', 
                        text:'Наши инновационные решения по системам биллинга предназначены для повышения эффективности управления и обслуживания Товариществ собственников жилья (ТСЖ), Жилищно-строительных кооперативов (ЖСК) и Жилищно-эксплуатационных управлений (ЖЭУ).'
                    },
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-02.png'), 
                        heading:'Управляющие организации', 
                        text:'Наша система предназначена для поддержки управляющих компаний в решении разнообразных задач, связанных с финансовым учетом, техническим обслуживанием и взаимодействием с жильцами.'
                    },
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-03.png'), 
                        heading:'Расчетные центры', 
                        text:'Наша система предназначена для обеспечения эффективного управления финансовыми потоками, точных расчетов и высокого уровня автоматизации.'
                    },
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-04.png'), 
                        heading:'Региональные операторы по обращению с ТБО ', 
                        text:'Мы предоставляем современные решения, специально разработанные для оптимизации и улучшения процессов управления и переработки ТБО в вашем регионе.'
                    },
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-05.png'), 
                        heading:'Теплосети', 
                        text:'Мы предоставляем интегрированные решения, направленные на эффективное управление и обеспечение надежной работы теплосетевых систем.'
                    },
                    {
                        icon: require('../assets/img/icons/aeroland-payment-box-icon-06.png'), 
                        heading:'Водоканалы', 
                        text:'Мы предоставляем комплексные решения для оптимизации работы водоканальных систем, обеспечивая эффективное управление и надежное обеспечение водоснабжения в вашем регионе.'
                    },
                ]
            }
        }
    }
</script>
