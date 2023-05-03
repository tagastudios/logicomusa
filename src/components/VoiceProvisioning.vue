<template>
  <v-form>
    <v-container>

      <v-row no-gutters>
        <v-col cols="12">
          <h1 class="text-center">Voice Provisioning</h1>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <v-select :items="['Sprout','Item2','Item3']" label="Select a Partner" required></v-select>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <v-text-field :rules="accountRules" label="Account Number" required></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="6">
          <v-text-field label="First Name" required></v-text-field>
        </v-col>
        <v-col cols="6">
          <v-text-field label="Last Name" required></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="3">
          <v-text-field label="Address" required></v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field label="City" required></v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field label="State" required></v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field label="Zip" required></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="6">
          <v-text-field label="Contact Phone" required></v-text-field>
        </v-col>
        <v-col cols="6">
          <v-text-field label="Contact Email" required></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="4">
          <v-select :items="['Item1','Item2','Item3']" label="Customer Type" required></v-select>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Phone Number to Provision" required></v-text-field>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Sip Password" required></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="4">
          <v-select :items="['Item1','Item2','Item3']" label="Ported" required></v-select>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="4">
          <v-checkbox label="Bypass E911 Address Automation" value="Bypass" hide-details></v-checkbox>
        </v-col>
        <v-col cols="8">
          <v-alert variant="outlined" type="warning" prominent border="top">(By checking "Bypass E911 Address Automation" you agree to manually add this phone number and address to Bandwidth)</v-alert>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <v-btn type="submit" class="mt-2">PROVISION</v-btn>
        </v-col>
      </v-row>

    </v-container>
  </v-form>
</template>

<script>
export default {
  name: 'VoiceProvisioning',
  data() {
    return {
      accountRules: [
        value => {
          if (value) return true
          return 'Account Number is required.'
        }
      ]
    }
  }
}
</script>

<style scoped>



</style>