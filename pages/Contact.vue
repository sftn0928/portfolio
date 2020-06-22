<template>
  <div id="contactWrapper">
    <Title title="Contact" id="Contact" />
    <div class="fade-in-el" v-scroll-inview:fadeIn>
      <v-form
        class="contact-content"
        name="contactForm"
        action="https://docs.google.com/forms/d/e/1FAIpQLSdLS3bLAOutJ0GuU9YRHdMbb4pDFe6nVjYySt8dSWXdgu8c4w/formResponse"
        method="post"
      >
        <div class="form-group">
          <p>お名前</p>
          <v-text-field
            v-model="name"
            name="entry.2005620554"
            label="山田 太郎"
            outlined
          ></v-text-field>
          <p class="name-com comment" v-show="name == '' ? true : false">
            ※お名前を入力してください。
          </p>
        </div>
        <div class="form-group">
          <p>ご連絡先</p>
          <v-text-field
            v-model="adress"
            name="entry.1045781291"
            label="mall@example.com"
            outlined
          >
          </v-text-field>
          <p class="adress-com comment" v-show="isAddres">
            ※メールアドレスを入力してください。
          </p>
        </div>
        <div class="form-group">
          <p>お問い合せ内容</p>
          <v-textarea
            name="entry.839337160"
            outlined
            v-model="msg"
            rows="8"
            label="お気軽にお問い合せ下さい。"
          ></v-textarea>
          <p class="msg-com comment" v-show="msg == '' ? true : false">
            ※お問い合せ内容を入力してください。
          </p>
        </div>
        <div class="submit-btn">
          <v-btn
            class="submit-btn"
            name="sub"
            @click="submitForm"
            :disabled="available"
            >送信</v-btn
          >
        </div>
      </v-form>
    </div>
  </div>
</template>

<script>
import Title from "@/components/Title.vue";
export default {
  components: {
    Title
  },
  data() {
    return {
      fadeInOption: {
        delay: 2
      },
      name: "",
      adress: "",
      msg: "",
      isAdd: Boolean
    };
  },
  computed: {
    isAddres() {
      var regexp = /^[A-Za-z0-9]{1}[A-Za-z0-9_.-]*@{1}[A-Za-z0-9_.-]{1,}\.[A-Za-z0-9]{1,}$/;
      if (this.adress != "" && regexp.test(this.adress)) {
        this.isAdd = true;
        return false;
      } else {
        this.isAdd = false;
        return true;
      }
    },
    available() {
      return this.name != "" && this.isAdd && this.msg != "" ? false : true;
    }
  },
  methods: {
    submitForm() {
      document.contactForm.submit();
    }
  }
};
</script>

<style>
.contact-content {
  margin: 0 23%;
}
.form-group {
  margin: 40px 0 10px 0;
}

textarea {
  resize: none;
}

.submit-btn {
  text-align: center;
}
.comment {
  margin-bottom: 20px;
  color: rgb(253, 48, 21);
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
  .contact-title {
    font-size: 1.5em;
  }
}
</style>
