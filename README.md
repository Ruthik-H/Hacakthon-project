# Hacakthon-project
import React from "react";
import { View, Text, TouchableOpacity, StyleSheet } from "react-native";
import { useNavigation } from "@react-navigation/native";
import { StackNavigationProp } from "@react-navigation/stack";
import { RootStackParamList } from "../App";

type ProfileScreenNavProp = StackNavigationProp<RootStackParamList, "Tabs">;

export default function ProfileScreen() {
  const navigation = useNavigation<ProfileScreenNavProp>();

  return (
    <View style={styles.container}>
      {/* Fake search bar */}
      <TouchableOpacity
        style={styles.fakeSearch}
        onPress={() => navigation.navigate("Search")}
      >
        <Text style={{ color: "gray" }}>Search...</Text>
      </TouchableOpacity>
      <Text style={styles.text}>Profile Screen Content</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: { flex: 1, padding: 20 },
  fakeSearch: {
    backgroundColor: "#000000",
    padding: 12,
    borderRadius: 10,
    marginBottom: 20,
  },
  text: { fontSize: 18 },
});
