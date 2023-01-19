<script setup></script>

<template>
    <div id="app">
        <div class="content_container">
            <!-- todo fix image -->
            <div class="background_image_container"></div>
            <div class="info_container">
                <h1 class="title">
                    Shift the overall look and feel by adding these wonderful touches to furniture in your home
                </h1>
                <p class="text">
                    Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and
                    uninviting. I’ve got some simple tips to help you make any room feel complete
                </p>
                <div class="user_container">
                    <div class="user_image_container">
                        <img src="../src/images/avatar-michelle.jpg" alt="avatar" />
                    </div>
                    <div class="user_text_container">
                        <h3 class="user_name">Michelle Appleton</h3>
                        <p class="date">28 Jun 2020</p>
                    </div>
                    <!-- !here HTML -->
                    <div class="share_icon_container">
                        <img src="../src/images/icon-share.svg" alt="share icon" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
/* Colors */
$Very-Dark-Grayish-Blue: hsl(217, 19%, 35%);
$Desaturated-Dark-Blue: hsl(214, 17%, 51%);
$Grayish-Blue: hsl(212, 23%, 69%);
$Light-Grayish-Blue: hsl(210, 46%, 95%);

/* Custom Font */
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@500;700&display=swap');

/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Manrope', sans-serif;
    font-size: 13px;
}

#app {
    width: 100vw;
    height: 100vh;
    background-color: $Light-Grayish-Blue;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2rem 0px;
    overflow: hidden;
    .content_container {
        width: 90%;
        max-width: 500px;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: white;
        border-radius: 1rem;
        box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);

        /* img styles comes here */
        .background_image_container {
            width: 100%;
            height: 15rem;
            background-image: url('../src/images/drawers.jpg');
            background-size: cover;
            background-position: center 20%;
            background-repeat: no-repeat;
        }
        .info_container {
            width: 100%;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            text-align: start;
            line-height: 1.5;

            .title {
                font-size: 1rem;
                font-weight: 700;
                color: $Very-Dark-Grayish-Blue;
                margin-bottom: 1rem;
            }
            .text {
                font-size: 0.8rem;
                font-weight: 500;
                color: $Desaturated-Dark-Blue;
                margin-bottom: 1rem;
            }
            .user_container {
                display: flex;
                align-items: center;
                justify-content: flex-start;
                width: 100%;

                .user_image_container {
                    width: 3rem;
                    height: 3rem;
                    border-radius: 50%;
                    overflow: hidden;
                    margin-right: 1rem;
                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }
                }
                .user_text_container {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: flex-start;
                    .user_name {
                        font-size: 0.85rem;
                        font-weight: 700;
                        color: $Very-Dark-Grayish-Blue;
                    }
                    .date {
                        font-size: 0.8rem;
                        font-weight: 500;
                        color: $Grayish-Blue;
                    }
                }
                .share_icon_container {
                    width: 2rem;
                    height: 2rem;
                    border-radius: 50%;
                    background-color: $Light-Grayish-Blue;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    margin-left: auto;
                    cursor: pointer;
                    transition: all 0.1s ease-in-out;
                    user-select: none;
                    &:hover {
                        transform: scale(1.1);
                        background-color: hsl(208, 14%, 79%);
                    }
                    &:active {
                        transform: scale(0.98);
                        box-shadow: 0px 0px 10px 0px rgb(158, 158, 215);
                    }
                    img {
                        width: 1rem;
                        height: 1rem;
                    }
                }
            }
        }
    }
}
</style>
