<template>
    <div class="card">
        <div class="company">
            <div class="company-logo-wrapper">
                <img :src="companyIconSrc" alt="Company Logo">
            </div>
            <div class="company-name">
                {{ companyName }}
            </div>
        </div>
        <div class="content">
            {{ content }}
        </div>
        <div class="card-image" v-if="image">
            <img :src="image" alt="Card Image">
        </div>

        <div class="date_info">
            <div class="info_text">{{ date }}</div>
            <div class="views">
                <div class="view-number-wrapper">
                    <img :src="eyeIconSrc" alt="Card Image">
                    <div class="view-number">{{ viewNumber }}</div>
                </div>
                <div class="info_text">
                    <img :src="backIconSrc" alt="Card Image">
                </div>
            </div>
        </div>
    </div>
</template>
    
<script>
export default {
    props: {
        companyIconSrc: String,
        companyName: String,
        content: String,
        image: String,
        viewNumber: String,
        date: String
    },
    data() {
        return {
            backIconSrc: require('@/public/icons/back-icon.svg'),
            eyeIconSrc: require('@/public/icons/eye-icon.svg')
        };
    }
}
</script>
    
<style scoped>
.card {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.company {
    display: flex;
    align-items: center;
    gap: 10px;
    max-height: 60px;
}

.company-logo-wrapper {
    border-radius: 10px;
}

.company-logo-wrapper img {
    border-radius: 12px;
}

.company-name {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 20px;
}

.content {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 7;
    overflow: hidden;
    color: #D0D0D0;
    align-self: stretch;
    white-space: nowrap;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 20px;
    text-wrap: wrap;
    max-height: 140px;
}

.card-image img {
    width: 100%;
    max-width: 340px;
    height: auto;
    display: block;
    border-radius: 10px;
}

.card-image {
    border-radius: 10px;
}

.date_info {
    display: flex;
    justify-content: space-between;
    padding: 5px 6px;
    background: rgba(255, 255, 255, 0.02);
    border-radius: 10px;
}

.info_text {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    padding: 8px;
}

.views {
    display: flex;
    padding: 0 8px;
    gap: 5px;
}

.view-number-wrapper {
    display: flex;
    align-items: center;
    padding-right: 8px;
    gap: 6px;
}

.view-number {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}
</style>