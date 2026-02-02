# 🌍 Human Names Database (Normalized)

A structured database of first and last names categorized by country and gender. This repository automatically converts human-readable country files into a **normalized relational schema** optimized for **Dexie.js** and **IndexedDB**.

## 🚀 How It Works

1. Add or edit JSON files in the `/first-names` and `/last-names` folders.
2. Once you push your changes, a GitHub Action automatically runs.
3. The action merges all countries, removes duplicate names to save space, and assigns unique IDs to create a relational database.
4. Four JSON files are generated in the `/public` folder. You can then use the file upload button in the game to import these files.


---

## 📂 Project Structure

* **`/first-names/`**: Source files containing gendered first names for each country.
* **`/last-names/`**: Source files containing surnames for each country.
* **`/public/`**: **Generated save files (Do not edit manually)**.

---

## 🛠 How to Add a New Country

To add a new country (e.g., East Germany), create a new JSON file in the appropriate folder using the format below.

> **Note:** The `countryName` field is optional and for your own reference. The `countryId` is required; you can find it by hovering over the team flag or checking the URL address on team-specific pages in the game.

### 1. First Names (`/first-names/east-germany.json`)
````
{
  "countryName": "East Germany",
  "countryId": 111,
  "maleNames": ["Wolfgang", "Hans"],
  "femaleNames": ["Heidi", "Petra"]
}
````
### 1. Last Names (`/last-names/east-germany.json`)
````
{
  "countryId": 111,
  "names": ["Schmidt", "Müller"]
}
````
