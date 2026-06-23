# TubeTV - YouTube Companion for Android TV

TubeTV is a native, premium, remote-friendly YouTube companion application designed specifically for Android TV. Built entirely in Kotlin with Jetpack Compose for TV, Room local database persistence, and clean MVVM architecture.

It complies strictly with YouTube's official Terms of Service by using the official secure HTML5 YouTube Player embedded safely inside an optimized System WebView.

---

## 📺 Key Features

### 1. 🌟 YouTube-Style TV UI & Navigation
*   **Collapsible Sidebar Navigation:** Left-hand navigation panel that smoothly expands on focus, offering quick routes to Home, Search, Favorites, Settings, and Legal sections.
*   **Material 3 TV Components:** Dynamic colors (Vibrant Purple, Intense Red brand accents) and custom cards that scale and show bright borders on focus.
*   **Fluid D-Pad Focus Transitions:** Every card and button is carefully designed for D-Pad remote control interaction without requiring touch/mouse gestures.

### 2. 🔍 Dynamic Video Feed, Web Search & Mirrors
*   **Horizontal Category Chips:** Easily filter between Gaming, Music, and News categories with horizontal lists.
*   **Featured Hero Banner:** Displays an elegant, high-impact background gradient with instant play triggers for premium live events.
*   **Local Search & Manual URL Parser:** Quickly search local playlists or paste/enter any public YouTube URL manually; the parser automatically and safely extracts only the 11-character video ID.
*   **PikaShow & Netmirror Companion Portals:** Integrated custom, TV-optimized, remote-friendly streaming dashboards. Seamlessly load Netmirror servers or PikaShow online mirrors (with manual proxy inputs) directly on your TV. Supports D-pad hover states, custom red/gold focus rings, quick reload, and full web-history remote back navigation.

### 3. 🛡️ Parental Control & Privacy
*   **Parental PIN Lock:** Protect settings configurations or favorite playlists behind a locally stored 4-digit PIN lock. Features a dedicated virtual remote on-screen keypad.
*   **100% Offline Storage:** Room local database persists favorites, watch history (recents), and system preferences completely locally on the TV.

### 4. 🇮🇳 Hindi-Friendly Layout & Easy Localization
*   Dual-text subtitle guides (English alongside clean Hindi markers like `Home / मुख्य पृष्ठ` and `Search / खोजें`) to ensure comfortable use across Hindi-speaking regions.

---

## 🛠️ Architecture and Stack

*   **UI Framework:** Jetpack Compose for TV (Experimental Material 3 TV APIs)
*   **Architecture Pattern:** Model-View-ViewModel (MVVM) with Repository Pattern
*   **Data Storage:** SQLite Room database with Kotlin coroutine flows for reactive updates
*   **Playback Wrapper:** Hardware-accelerated Android `WebView` loaded with official `https://www.youtube.com/embed/VIDEO_ID` configuration parameters.

---

## ⚖️ Legal & Policy Compliance

*   **No Ad Blocking:** Integrates standard official iframe embed options; does not block or modify video monetization ads.
*   **No Background Playback:** WebView lifecycle suspends on-screen content rendering as soon as the playback screen loses focus or exits.
*   **No Downloading / Scraping:** No extraction of raw audio streams, web scraping, or unauthorized downloading of media.
