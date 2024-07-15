import React from 'react';
import { View, Text, TextInput, StyleSheet, ScrollView, Image, TouchableOpacity, Dimensions } from 'react-native';

const { width: viewportWidth } = Dimensions.get('window');

const crops = [
  { label: 'Crop 1' },
  { label: 'Crop 2' },
  { label: 'Crop 3' },
  { label: 'Crop 4' },
  { label: 'Crop 5' },
  { label: 'Crop 6' },
];

const newsItems = [
  { headline: 'Headline 1', description: 'Description 1', time: 'Today • 23 min' },
  { headline: 'Headline 2', description: 'Description 2', time: 'Today • 23 min' },
  { headline: 'Headline 3', description: 'Description 3', time: 'Today • 23 min' },
  { headline: 'Headline 4', description: 'Description 4', time: 'Today • 23 min' },
  { headline: 'Headline 5', description: 'Description 5', time: 'Today • 23 min' },
];

const App = () => {
  const renderCropItem = (item, index) => (
    <View key={index} style={styles.miniCard}>
      <Image style={styles.miniCardImage} />
      <Text style={styles.miniCardLabel}>{item.label}</Text>
    </View>
  );

  const renderNewsItem = (item, index) => (
    <TouchableOpacity key={index} style={styles.newsCard}>
      <Image style={styles.newsCardImage} />
      <View style={styles.newsCardTextContainer}>
        <Text style={styles.newsCardHeadline}>{item.headline}</Text>
        <Text style={styles.newsCardDescription}>{item.description}</Text>
        <Text style={styles.newsCardTime}>{item.time}</Text>
      </View>
    </TouchableOpacity>
  );

  return (
    <View style={styles.container}>
      {/* Header */}
      <View style={styles.header}>
        <TouchableOpacity>
          <Image style={styles.icon} source={{ uri: 'https://example.com/profile-icon.png' }} />
        </TouchableOpacity>
        <Text style={styles.time}>9:30</Text>
        <TouchableOpacity>
          <Image style={styles.icon} source={{ uri: 'https://example.com/notification-icon.png' }} />
        </TouchableOpacity>
      </View>

      <ScrollView style={styles.scrollContainer}>
        {/* Search Bar */}
        <View style={styles.searchBar}>
          <TextInput style={styles.input} placeholder="Input text" />
        </View>

        {/* Ask Query */}
        <View style={styles.section}>
          <Text style={styles.sectionTitle}>Ask Query</Text>
          <TouchableOpacity style={styles.card}>
            <Image style={styles.cardImage} />
            <Text style={styles.cardLabel}>1st</Text>
          </TouchableOpacity>
        </View>

        {/* Crop */}
        <View style={styles.section}>
          <Text style={styles.sectionTitle}>Crop</Text>
          <ScrollView horizontal>
            {crops.map((item, index) => renderCropItem(item, index))}
          </ScrollView>
        </View>

        {/* FAQs */}
        <View style={styles.section}>
          <Text style={styles.sectionTitle}>FAQs</Text>
          <ScrollView horizontal>
            <TouchableOpacity style={styles.faqCard}>
              <Image style={styles.faqCardImage} />
              <Text style={styles.faqCardText}>Artist</Text>
              <Text style={styles.faqCardText}>Song</Text>
            </TouchableOpacity>
            <TouchableOpacity style={styles.faqCard}>
              <Image style={styles.faqCardImage} />
              <Text style={styles.faqCardText}>Artist</Text>
              <Text style={styles.faqCardText}>Song</Text>
            </TouchableOpacity>
            <TouchableOpacity style={styles.faqCard}>
              <Image style={styles.faqCardImage} />
              <Text style={styles.faqCardText}>Artist</Text>
              <Text style={styles.faqCardText}>Song</Text>
            </TouchableOpacity>
          </ScrollView>
        </View>

        {/* News */}
        <View style={styles.section}>
          <Text style={styles.sectionTitle}>News</Text>
          <ScrollView horizontal>
            {newsItems.map((item, index) => renderNewsItem(item, index))}
          </ScrollView>
        </View>
      </ScrollView>

      {/* Footer */}
      <View style={styles.footer}>
        <TouchableOpacity style={styles.footerButton}>
          <Text style={styles.footerButtonText}>Home</Text>
        </TouchableOpacity>
        <TouchableOpacity style={styles.footerButton}>
          <Text style={styles.footerButtonText}>My Farm</Text>
        </TouchableOpacity>
        <TouchableOpacity style={styles.footerButton}>
          <Text style={styles.footerButtonText}>Profile</Text>
        </TouchableOpacity>
      </View>
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#f5f5f5',
  },
  header: {
    flexDirection: 'row',
    justifyContent: 'space-between',
    alignItems: 'center',
    paddingHorizontal: 15,
    paddingTop: 10,
  },
  time: {
    fontSize: 20,
  },
  icon: {
    width: 20,
    height: 20,
    borderRadius: 10,
  },
  searchBar: {
    padding: 15,
    backgroundColor: '#fff',
  },
  input: {
    backgroundColor: '#f0f0f0',
    padding: 10,
    borderRadius: 8,
  },
  scrollContainer: {
    flex: 1,
  },
  section: {
    padding: 15,
  },
  sectionTitle: {
    fontSize: 18,
    fontWeight: 'bold',
    marginBottom: 10,
  },
  card: {
    backgroundColor: '#e0e0e0',
    borderRadius: 10,
    padding: 20,
    alignItems: 'center',
  },
  cardImage: {
    width: 100,
    height: 100,
    backgroundColor: '#d0d0d0',
    borderRadius: 10,
  },
  cardLabel: {
    marginTop: 10,
    fontSize: 16,
  },
  miniCard: {
    backgroundColor: '#e0e0e0',
    borderRadius: 10,
    padding: 10,
    alignItems: 'center',
    marginRight: 10,
  },
  miniCardImage: {
    width: 50,
    height: 50,
    backgroundColor: '#d0d0d0',
    borderRadius: 10,
  },
  miniCardLabel: {
    marginTop: 5,
    fontSize: 14,
  },
  faqCard: {
    backgroundColor: '#e0e0e0',
    borderRadius: 10,
    padding: 20,
    marginRight: 10,
    alignItems: 'center',
  },
  faqCardImage: {
    width: 100,
    height: 100,
    backgroundColor: '#d0d0d0',
    borderRadius: 10,
  },
  faqCardText: {
    marginTop: 10,
    fontSize: 16,
  },
  newsCard: {
    flexDirection: 'row',
    backgroundColor: '#e0e0e0',
    borderRadius: 10,
    padding: 15,
    marginBottom: 10,
    marginRight: 10,
  },
  newsCardImage: {
    width: 80,
    height: 80,
    backgroundColor: '#d0d0d0',
    borderRadius: 10,
  },
  newsCardTextContainer: {
    marginLeft: 15,
    flex: 1,
  },
  newsCardHeadline: {
    fontSize: 16,
    fontWeight: 'bold',
  },
  newsCardDescription: {
    fontSize: 14,
    marginVertical: 5,
  },
  newsCardTime: {
    fontSize: 12,
    color: '#777',
  },
  footer: {
    flexDirection: 'row',
    justifyContent: 'space-around',
    paddingVertical: 10,
    backgroundColor: '#fff',
  },
  footerButton: {
    padding: 10,
  },
  footerButtonText: {
    fontSize: 16,
  },
});

export default App;
