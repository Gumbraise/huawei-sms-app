<template>
  <message-list :xml="xml"/>
</template>

<script>
import messageList from "./messages-card/messageList";
let parser = require('fast-xml-parser');

export default {
  name: 'messages',
  components: {
    messageList,
  },
  data() {
    return {
      xml: '',
    }
  },
  mounted() {
    let xmlData = "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
        "<response>\n" +
        "    <Count>6</Count>\n" +
        "    <messages>\n" +
        "        <message>\n" +
        "            <smstat>0</smstat>\n" +
        "            <index>40019</index>\n" +
        "            <phone>22850</phone>\n" +
        "            <content>Info Bouygtel: vous avez atteint la date de fin de validité de votre forfait additionnel de 30 Go.\n" +
        "            </content>\n" +
        "            <date>2021-08-21 09:02:37</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>1</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "        <message>\n" +
        "            <smstat>1</smstat>\n" +
        "            <index>40018</index>\n" +
        "            <phone>+33771801718</phone>\n" +
        "            <content>Yoww</content>\n" +
        "            <date>2021-08-18 13:05:18</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>1</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "        <message>\n" +
        "            <smstat>1</smstat>\n" +
        "            <index>40014</index>\n" +
        "            <phone>Bouygtel</phone>\n" +
        "            <content>Un incident a été détecté sur votre secteur et peut potentiellement impacter vos services Bbox. Par\n" +
        "                précaution, nous allons ajouter une recharge gratuite de 30 Go à votre forfait mobile afin de vous\n" +
        "                garantir une continuité de service. Pour utiliser pleinement cette recharge, c&apos;est ici : bytl.fr&#x2F;Internet-garanti.\n" +
        "                Soyez assuré que nos équipes techniques sont mobilisées pour régler cet incident dans les plus brefs\n" +
        "                délais. Nous vous prions de nous excuser pour la gene occasionnée. Sous réserve d&apos;offre compatible,\n" +
        "                vous recevrez sous 2 heures un SMS de confirmation de la mise en place de la recharge. Vous pourrez\n" +
        "                suivre sa consommation sur votre espace client. Merci de votre confiance.\n" +
        "            </content>\n" +
        "            <date>2021-08-06 13:00:11</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>2</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "        <message>\n" +
        "            <smstat>1</smstat>\n" +
        "            <index>40011</index>\n" +
        "            <phone>0660660001</phone>\n" +
        "            <content>Vous avez 1 nouveau message. Consultez le 660</content>\n" +
        "            <date>2021-07-28 12:21:52</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>1</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "        <message>\n" +
        "            <smstat>1</smstat>\n" +
        "            <index>40010</index>\n" +
        "            <phone>AUTHMSG</phone>\n" +
        "            <content>Votre code de vérification BitClout est: 773360</content>\n" +
        "            <date>2021-07-26 12:49:26</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>1</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "        <message>\n" +
        "            <smstat>1</smstat>\n" +
        "            <index>40004</index>\n" +
        "            <phone>0986371653</phone>\n" +
        "            <content>Le 11&#x2F;07&#x2F;2021 à 15:51, ce correspondant a cherché à vous joindre 1 fois sans laisser de\n" +
        "                message.\n" +
        "            </content>\n" +
        "            <date>2021-07-11 15:51:53</date>\n" +
        "            <sca></sca>\n" +
        "            <savetype>0</savetype>\n" +
        "            <priority>0</priority>\n" +
        "            <smstype>1</smstype>\n" +
        "            <unreadcount>0</unreadcount>\n" +
        "        </message>\n" +
        "    </messages>\n" +
        "</response>"

    try {
      let yo = parser.parse(xmlData, '', true);
      this.xml = yo.response.messages.message
    } catch (error) {
      console.log(error.message)
    }
  },
}
</script>

<style scoped>

</style>