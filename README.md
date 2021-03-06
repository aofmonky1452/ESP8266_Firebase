# ESP8266_Firebase

### Create & Update ###
Firebase.setInt(firebaseData, "...path...", value);


# === Example 1 ===
Firebase.setInt(firebaseData, "path1", 100);

# === Example 2 ===
int x = 100;
Firebase.setInt(firebaseData, "path1/sub1", x);






### Read ###
if(Firebase.getInt(firebaseData, "...path...")) {
  if(firebaseData.dataType() == "int") {
    Serial.println(firebaseData.intData());
  }
}
else {
  Serial.println(firebaseData.errorReason());
}

# ==== Example ====
int x;
if(Firebase.getInt(firebaseData, "path1")) {
  if(firebaseData.dataType() == "int") {
    Serial.println(firebaseData.intData());
    x = firebaseData.intData();
  }
}
else {
  Serial.println(firebaseData.errorReason());
}








