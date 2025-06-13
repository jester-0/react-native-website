import React from 'react';
import { SafeAreaView, View, Text, Button, StyleSheet } from 'react-native';

export default function App() {
  const [count, setCount] = React.useState(0);

  return (
    <SafeAreaView style={styles.container}>
      <Text style={styles.header}>Привет 👋</Text>
      <Text style={styles.text}>Счетчик: {count}</Text>
      <View style={styles.buttonContainer}>
        <Button title="Увеличить" onPress={() => setCount(count + 1)} />
        <Button title="Сбросить" onPress={() => setCount(0)} color="#999" />
      </View>
    </SafeAreaView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    padding: 20,
    backgroundColor: '#f4f4f4',
  },
  header: {
    fontSize: 24,
    fontWeight: 'bold',
    marginBottom: 20,
  },
  text: {
    fontSize: 18,
    marginBottom: 20,
  },
  buttonContainer: {
    width: '100%',
    gap: 10,
  },
});

