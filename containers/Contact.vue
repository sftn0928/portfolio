<template>
    <div id="contactWrapper">
        <Title title="Contact" id="Contact" />
        <h3 class="contact-title">お問い合せ</h3>
        <form class="contact-content" name="contactForm"
         action="https://docs.google.com/forms/d/e/1FAIpQLSdLS3bLAOutJ0GuU9YRHdMbb4pDFe6nVjYySt8dSWXdgu8c4w/formResponse"
         method="post">
            <div class="form-group">
                <p>お名前</p>
                <input type="text" v-model="name" name="entry.2005620554" class="form-control"
                 placeholder="山田 太郎" rule="required" >
                <p class="name-com comment" v-show="name_comment">※お名前を入力してください。</p>
            </div>
            <div class="form-group">
                <p>ご連絡先</p>
                <input type="email" v-model="adress" name="entry.1045781291" class="form-control"
                 placeholder="mall@example.com" rule="required">
                <p class="adress-com comment" v-show="adress_comment">※メールアドレスを入力してください。</p>

            </div>
            <div class="form-group">
                <p>お問い合せ内容</p>
                <textarea name="entry.839337160" v-model="msg" rows="8" class="form-control"
                 placeholder="お気軽にお問い合せ下さい。" rule="required" ></textarea>
                <p class="msg-com comment" v-show="msg_comment">※お問い合せ内容を入力してください。</p>
            </div>
                <p class="submit-p"><input type="button" value="送信" class="submit btn btn-outline-info"
                 name="sub"  @click="submit_form" v-if="available"></p>
                    <!-- ダミーボタン -->
                <p class="submit-p"><input type="button" value="送信" class="submit btn btn-outline-info"
                 v-if="!available"></p>

        </form>
    </div>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    components: {
        Title
    },
    data() {
        return {
            name: '',
            adress: '',
            msg: ''
        }
    },

    computed: {
        name_comment: function() {
            if(this.name == "") {
                return true;
            }
            else {
                return false;
            }
        },
        adress_comment: function() {
            if(this.adress == "") {
                return true;
            }
            else {
                return false;
            }
        },
        msg_comment: function() {
            if(this.msg == "") {
                return true;
            }
            else {
                return false;
            }
        },
        available: function() {
            if(this.name != "" && this.adress != "" && this.msg != "" ) {
                return true;
            }
            else {
                return false;
            }
        }
    },
    methods: {
        submit_form: function() {
            document.contactForm.submit();
        }
    }
}

</script>

<style>
.contact-title{
    text-align: center;
    margin: -20px 0 30px 0;
}

.contact-content {
    margin: 0 20%;
}

.form-group {
    margin: 40px 0 10px 0;
}

textarea{
    resize: none;
}

.submit {
    cursor: pointer;
    width: 100px;
    margin-bottom: 10px;
}

.submit-p {
    text-align: center;
}

.comment {
    margin-bottom: 20px;
    color: rgb(253, 48, 21);
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .contact-title{
        font-size:  1.5em;
    }
}

</style>