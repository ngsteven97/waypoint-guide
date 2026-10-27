# Waypoint Guide

Waypoint is a live departures board for your desk, shelf or wall. It shows real-time **trains, buses and Tube services**, the **aircraft flying overhead**, and **satellites passing over your home**, all on a crisp OLED display.

This guide takes you from the box to a working board in about ten minutes.

<img width="1772" height="982" alt="IMG_0293" src="https://github.com/user-attachments/assets/7ea9d35d-e186-4d52-a229-3d169c012749" />

## Quick start

1. **Plug it in** to a USB power supply.
2. **Join the "Waypoint" Wi-Fi network** on your phone and tell the board your home Wi-Fi details.
3. **Open the setup page** in your browser and run the **Setup Wizard** with your postcode. Based on your postcode, it should find all your local services and pinpoint your location for plane/satellite tracking.
4. **Enter your API keys** Paste in your API keys for the relevant services that you want.
6. Reboot and done! Use the **touch button** to flip between stations and modes.

The rest of this guide walks through each step with pictures.

---

## Contents

1. [What you need](#1-what-you-need)
2. [Plug in your Waypoint](#2-plug-in-your-waypoint)
3. [Connect to Wi-Fi](#3-connect-to-wi-fi)
4. [Open the setup page](#4-open-the-setup-page)
5. [Run the Setup Wizard](#5-run-the-setup-wizard)
6. [Getting your API keys](#6-getting-your-api-keys)
7. [Using the touch button](#7-using-the-touch-button)
8. [Changing things later](#8-changing-things-later)
9. [Updates](#9-updates)
10. [FAQ](#10-faq)
11. [Troubleshooting](#11-troubleshooting)
12. [Resetting your Waypoint](#12-resetting-your-waypoint)
13. [Support](#13-support)

---

## 1. What you need

- Your Waypoint
- A USB power supply and cable (your Waypoint uses a 5V supply, so requires an old-school USB-A to USB-C cable!)
- A **2.4 GHz Wi-Fi network** and its password. Waypoint can't use 5 GHz-only networks. Most home routers broadcast both, so you don't normally need to do anything.
- A phone, tablet or computer on the same Wi-Fi network

<img width="2364" height="966" alt="back" src="https://github.com/user-attachments/assets/503e60e2-5604-42a0-a927-cae5bc266497" />

> Note: there may be minor differences to the design of the 3D printed enclosure depending on the order batch - don't worry, the hardware will remain exactly the same and your Waypoint will work as intended!

Train times need an API key from National Rail (see [section 6](#6-get-a-rail-key-train-times-only)). 
Normal operation of Buses, Tube, aircraft and satellites need no keys at all.
There is an optional API key for OpenWeather to display the weather on the screen.
There is also an optional API key for RapidAPI flight tracking to track a live flight.

---

## 2. Plug in your Waypoint

Connect the power. After a moment the display lights up with a short animated splash.

> **Tip:** try not to touch the touch sensor during the first couple of seconds after power-up. Touching it during the splash starts the factory-reset countdown (see [section 12](#12-resetting-your-waypoint)). Letting go straight away cancels it.

---

## 3. Connect to Wi-Fi

A brand-new Waypoint doesn't know your Wi-Fi yet, so it creates a little Wi-Fi network of its own that you use to tell it.

**1.** After the splash, the display shows **"Waypoint first-time setup"**:

<img width="5712" height="3213" alt="setup" src="https://github.com/user-attachments/assets/51c690af-9968-4f5b-9fd7-51bc3c932874" />

<p>&nbsp;</p>

<img align="right" width="374" alt="Waypoint Wi-Fi network in the Windows Wi-Fi list" src="https://github.com/user-attachments/assets/4777da9e-a4ba-4356-b64f-f9945a868997" />

**2.** On your phone/laptop/tablet/PC, open **Wi-Fi settings** and join the network called **Waypoint**. There's no password.

<br clear="right">
<p>&nbsp;</p>

**3.** A setup page should open by itself. If it doesn't, open a web browser and go to **http://192.168.4.1**.

<img width="1143" height="860" alt="image" src="https://github.com/user-attachments/assets/9be8f6fd-f39e-4608-82fb-b35df4863257" />

<p>&nbsp;</p>

<img align="right" width="470" alt="Wi-Fi setup page with SSID and password fields" src="https://github.com/user-attachments/assets/4362b08c-a522-44c9-a277-154b36545df6" />

**4.** Tap **Configure WiFi**, choose your home network from the list and type its password. Then tap **Save**.

<br clear="right">

<p>&nbsp;</p>

<img align="right" width="415" alt="Saving credentials message" src="https://github.com/user-attachments/assets/88aad584-5b8e-4ac8-859c-f7f0026a50b7" />

**5.** Waypoint connects to your network. When it works, the display shows **"Wi-Fi Connected"** along with the board's **IP address** in the corner. Make a note of it; you may need it in the next step.

<br clear="right">

<p>&nbsp;</p>

---

## 4. Open the setup page

Now that Waypoint is on your home network, make sure your phone or computer is on the **same network** and open a browser.

Type **http://waypoint.local** and press Go.

If that doesn't load (some phones and routers don't support `.local` addresses), type the **IP address from the display** instead, for example `http://192.168.1.50`.

The display now shows **"Waypoint Setup – Complete setup in your browser"**, with the address to use:

<img width="2364" height="1330" alt="ip address" src="https://github.com/user-attachments/assets/4a568db9-b45a-450c-bc18-8a76d9441698" />

The page automatically opens the **Setup Wizard**.

---

## 5. Run the Setup Wizard

The wizard has four steps and sets up all of Waypoint's modes in one go. You can rerun it whenever you like using the **🧭 Setup Wizard** button at the top of the page.

### Step 1: Location

Type your **postcode** and tap **Find Stops**. Waypoint uses it to find your nearest stations and stops, to centre the aircraft and satellite tracking on your home, and for local weather.

<img width="1688" height="597" alt="image" src="https://github.com/user-attachments/assets/5c597924-6e3d-4643-8286-66d876f69fbd" />

### Step 2: Confirm and configure

Check the suggestions and change anything that isn't right.

<img align="right" width="70%" alt="Waypoint setup screen" src="https://github.com/user-attachments/assets/2437e316-4a5c-4bc8-82e1-0993370b783e" />

- **Nearest train station**: pick one, or **Skip**.
- **Nearest Tube / DLR / Elizabeth line station**: pick one, or **Skip** if you don't use them.
- **Nearest bus stop**: pick one, or **Skip**.
- **Air mode**: how Waypoint looks for aircraft near you.
- **Space mode**: choose which satellites to look for (space stations, Starlink, weather satellites and more).
- **Weather**: switch on to show the temperature and conditions. This needs a free OpenWeatherMap key (next step).
- **Hostname**: the name in `waypoint.local`. Leave it as it is unless you have more than one Waypoint.
- **Flip Display**: turn this on if the unit sits upside-down.
- **Sleep Mode**: blanks the display overnight between the hours you choose.
- **Firmware updates**: leave both ticked and Waypoint keeps itself up to date.

<br clear="right">

### Step 3: API keys

<img width="1696" height="1271" alt="image" src="https://github.com/user-attachments/assets/2ee5319d-23f7-45a5-9c29-ff55e0e7f777" />


An API key is a free password that a data provider gives you so Waypoint can fetch their data. Which ones you need depends on what you want Waypoint to show. You can paste keys in here, or leave the boxes blank and add them later under **⚙ Settings → API Keys**.

| Key | Required? | Needed for | How to get it |
|---|---|---|---|
| **Rail Data Marketplace key** | **Required for train times** | Train departures | [Steps below](#rail-data-marketplace-key-train-times) |
| **OpenWeatherMap key** | Optional | Weather on the display | [Steps below](#openweathermap-key-weather) |
| **TfL key** | Optional (recommended) | Smoother Tube and bus lookups | [Steps below](#tfl-key-tube-and-bus) |![Uploading 192.168.3.181_setup.png…]()

| **RapidAPI key** | Optional | Flight Watch scheduled times | [Steps below](#rapidapi-key-flight-watch) |

Buses, Tube, aircraft and satellites all work without any key at all.

### Step 4: Default mode

<img width="1368" height="1624" alt="192 168 3 181_setup" src="https://github.com/user-attachments/assets/2c08ca77-a152-4164-a2b9-bdc02f789a7e" />

- **Modes This Board Uses**: untick anything you don't want. The touch button will skip those modes.
- **Default board mode**: Ground (trains, buses, Tube), Air (planes) or Space (satellites). This is what Waypoint starts in.
- **Ground sub-mode**: if you chose Ground, pick Rail, Tube, Bus or Combined. *Combined* mixes all three into one board, sorted by time.

Tap **Apply Everything to Board**. Your first departures will appear on the display shortly after.

> Each mode can hold up to **four** stations or stops. The wizard sets up the first one. You can add more later (see [section 8](#8-changing-things-later)) and flip between them with a tap.

---

## 6. Getting your API keys

Each key below is free, and each has its own short set of steps. Only the **Rail** key is needed for a standard setup; the rest are optional extras.

**Where to paste a key:** open your Waypoint page, go to **⚙ Settings**, find the **API Keys** box, paste the key into the matching field and tap **💾 Save API Keys**. Reboot afterwards (**🖥 System → ⟳ Reboot**) so the new key is picked up. You can also paste keys straight into step 3 of the Setup Wizard.

---

### Rail Data Marketplace key (train times)

**Required if you want train departures.** Takes about five minutes.

1. Go to [raildata.org.uk](https://raildata.org.uk) and **sign up** for a free account.
2. Open the **Data Product Catalogue**.
3. Search for **LDBWS**.
4. Choose **Live Departure Board (Public)** (also listed as *Live Departure Board 1.1*) and **subscribe**.
5. Accept the licence.
6. Open **My Subscriptions** and select your new subscription.
7. Go to the **Specification** tab and copy the **Consumer key**. Copy the *key*, not the *secret*.
8. In Waypoint, set **National Rail Feed** to **Rail Delivery Group feeds (recommended)**, paste the key into **Rail Data Marketplace API Key** and save.

Until Waypoint has a Rail key, a unit set to show trains stays on its setup screen. Once the key is saved, it restarts by itself.

> **Already have an older National Rail "Darwin" token?** (It looks like `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`.) Choose **Legacy OpenLDBWS** as the feed and paste it in. New Darwin tokens are no longer issued, so most people should use the Rail Data Marketplace key above.

---

### OpenWeatherMap key (weather)

**Optional.** Only needed if you switch on the weather display.

1. Go to [openweathermap.org](https://home.openweathermap.org/users/sign_up) and **sign up** for a free account.
2. Open the confirmation email and **confirm your address**.
3. Sign in and open the **API keys** tab.
4. Copy the **default key** (a 32-character string of letters and numbers).
5. In Waypoint, paste it into **OpenWeatherMap API Key** and save.

The free "Current Weather" tier is plenty. **New keys can take up to a couple of hours to start working.** If Waypoint reports an invalid key straight after you sign up, wait a while and try again.

---

### TfL key (Tube and bus)

**Optional, but recommended.** The Tube and bus services work without a key, but a key makes it less likely that lookups are slowed or refused when TfL is busy.

1. Go to the [TfL API portal](https://api-portal.tfl.gov.uk/signup) and **sign up** for a free account.
2. Open **Products**.
3. Choose **500 Requests per min**.
4. Enter a name for the subscription (anything you like, for example "Waypoint") and tap **Subscribe**.
5. Open your **Profile** and tap **Show key** to reveal your key (32 characters).
6. In Waypoint, paste it into **TfL API Key** and save.

---

### RapidAPI key (Flight Watch)

**Optional.** Flight Watch tracks one particular flight. Without a key it still works if you enter the departure and arrival details yourself. With a key, Waypoint can fetch the scheduled times automatically when you enter a flight number.

1. Go to [rapidapi.com](https://rapidapi.com) and **sign up** or sign in.
2. Search for **AeroDataBox** and open its API page.
3. Open the **Pricing** tab and subscribe to the free **Basic** plan.
4. Open any endpoint on the API page and copy the **X-RapidAPI-Key** value from the sample code snippet.
5. In Waypoint, paste it into the RapidAPI key field and save.

The free plan has a small quota, but it's plenty for occasional Flight Watch lookups.

<p>
<img height="220" alt="Flight tracking 1" src="https://github.com/user-attachments/assets/1a4c01e5-c671-4458-a51e-af2d10e0454d" /> <img height="220" alt="Flight tracking 2" src="https://github.com/user-attachments/assets/31686791-dcbd-483f-ae20-9b9dcea47445" />
</p>

---

## 7. Using the touch button

Waypoint has no screen buttons. Instead, there is a **touch sensor** you just tap or hold with a finger. This can be found on the left side of the unit.

- **Tap**: touch and let go quickly.
- **Hold**: keep your finger on it for about half a second or more.
- When Waypoint asks you to **hold to confirm**, a progress bar appears. Keep holding until it fills, or let go to cancel.

### Trains, buses and Tube

| Do this | And this happens |
|---|---|
| **Tap** | Show the next station or stop you've set up. A banner shows which one (for example *Slot 2/3*). |
| **Hold** | Switch between **Rail → Bus → Tube → Combined**. |
| **Keep holding** | A **"Switch to Air Mode"** prompt appears. Keep holding to confirm, or let go to stay put. |

<img width="2364" height="1330" alt="ground to air" src="https://github.com/user-attachments/assets/7c4c40a4-ae02-4e4d-bd4e-56379818e97b" />

### Aircraft (Air mode)

| Do this | And this happens |
|---|---|
| **Tap** | Flip through the details of each plane overhead, and back to the list. |
| **Hold** | "Switch to Space Mode" prompt. Keep holding to confirm. |

If you're tracking a specific flight with **Flight Watch**, a tap switches between the progress bar and the live panel, and a hold lets you cancel tracking.

<img width="2364" height="1330" alt="air to space" src="https://github.com/user-attachments/assets/93ebf2b4-7c12-4401-9711-c856eb4d6b33" />

### Satellites (Space mode)

| Do this | And this happens |
|---|---|
| **Tap** | Flip through the satellites overhead, and back to the list. |
| **Hold** | "Switch to Ground Mode" prompt. Keep holding to confirm. |

<img width="2364" height="1330" alt="space to ground" src="https://github.com/user-attachments/assets/54df5159-75ff-4ffa-9d12-6568a8caa55e" />

The hold cycle goes **Ground → Air → Space → Ground**. Any mode you've turned off is skipped.

You can also switch modes from the **Ground / Air / Space** tabs at the top of the Waypoint web page.

---

## 8. Changing things later

Open **http://waypoint.local** (or the IP address) any time to change settings. There are different Waypoint pages depending on what mode you are currently in, so the tabs you see will vary. Use the **🚉 Ground / ✈ Air / 🛸 Space** buttons at the top of the page to jump between modes.

<p>
<img width="32%" alt="Ground mode web page" src="https://github.com/user-attachments/assets/3d5a0eb4-ff09-4d90-9f52-5c54051e317e" /> <img width="32%" alt="Air mode web page" src="https://github.com/user-attachments/assets/8869048c-5f39-4ef5-a1c5-082bc0ca1c49" /> <img width="32%" alt="Space mode web page" src="https://github.com/user-attachments/assets/c3e5b77c-6979-4384-9475-7ff678ec0155" />
</p>

### 🚉 Ground mode (trains, buses and tubes)

- **🚂 Rail**: add up to four stations. Filter by platform or by a station the train calls at, and add a walking-time offset so you only see trains you can still catch.
- **🚌 Bus**: add up to four stops. Search by name or postcode, and optionally filter by route number.
- **🚇 Tube**: add up to four stations. Filter by line and direction.
- **⊞ Combined**: merge Rail, Bus and Tube slots into one board, sorted by departure time.

### ✈ Air mode (aircraft overhead)

- **✈ Air**: set where Waypoint looks (search for a postcode or enter coordinates), how far out it scans, your preferred units (aviation, imperial or metric), and how close a plane has to get before the full-detail view appears. A live scan preview shows what's overhead right now.
- **🎯 Flight Watch**: enter a flight number to follow one particular flight. The display shows its progress, altitude and speed while it's in range. Adding a free RapidAPI key in Settings lets Waypoint look up the scheduled times for you.

### 🛸 Space mode (satellites overhead)

- **🛸 Space**: set your location, choose which satellites to track (space stations, Starlink, weather, amateur radio, Galileo and others), and adjust when the detail view appears. A live preview shows what's overhead right now.
- **🎯 Sat Watch**: track one satellite by its NORAD number (the ISS is 25544). The display shows its altitude, speed, position in the sky and the country or ocean it's currently over.

### On every mode

- **⚙ Settings**: choose which modes to use, set brightness and scroll speed, flip the display, set sleep hours, weather, hostname, timezone (if you're outside the UK) and API keys. Tap **💾 Save Settings** when you're done.
- **🖥 System**: reboot, check for and install firmware updates, back up or restore your settings, erase Wi-Fi, factory reset, and see how well Waypoint is running (signal strength, uptime, free memory and so on).
- **📖 Guide**: a built-in version of this setup guide, plus a **🧭 Setup Wizard** that finds your nearest stops and configures the board for you.

It's a good idea to tap **Backup Config** on the System tab once you're happy with your setup.

---

## 9. Updates

Waypoint updates itself over the internet. By default it checks when it starts and once a night, and installs new versions automatically.

To update by hand: open the **🖥 System** tab, tap **↑ Install Firmware Update**, pick a version and tap **⬆ Install Selected**. Watch the display for progress. Waypoint restarts when it's finished.

> **Don't unplug it while it's updating.**

---

## 10. FAQ

**Do I need to pay for anything or subscribe to anything?**
No ongoing fees come with Waypoint itself. The data providers it uses are free, but train times need you to register for a free key (section 6). Weather needs a free OpenWeatherMap key if you want it.

**Do I need an app?**
No. Everything is done in a web browser on your phone or computer. You only need to be on the same Wi-Fi as Waypoint.

**Does it work outside the UK?**
Air and Space modes work anywhere. Trains, buses and the Tube use UK data. The data will still be live data, but might not help you get the train if it's 500 miles away! Set your timezone under Settings if you're outside the UK (for the clock.)

**Can I use it with 5 GHz Wi-Fi?**
Waypoint needs a 2.4 GHz network. If your router has separate names for 2.4 and 5 GHz, choose the 2.4 GHz one.

**Can it show more than one station?**
Yes: up to four stations, four bus stops and four Tube stations. Tap the touch sensor to flip between them. The **Combined** mode can also merge trains, buses and Tube into a single board.

**What does "Combined" mean?**
It's a board that mixes your trains, buses and Tube services into one list sorted by departure time.

**Is the screen a touchscreen?**
No. The display only shows information. The touch sensor is the separate button on the unit.

**Will the display burn in?**
OLED screens can wear if a picture is on all the time. To keep it looking great, turn on **Sleep Mode** (so it blanks overnight) and keep **Brightness** modest in Settings.

**What happens after a power cut?**
Waypoint remembers its settings. When the power returns, it restarts and reconnects to your Wi-Fi on its own.

**I changed my router or Wi-Fi password.**
Waypoint can't connect, so it brings back its own **Waypoint** network after a short wait. Join it and repeat [section 3](#3-connect-to-wi-fi). Your other settings are kept.

**The picture is upside-down.**
Open **⚙ Settings** and switch **Flip Display** on.

**Can I have two Waypoints in the same home?**
Yes. Give each a different name under **Hostname** (for example `waypoint-kitchen`) so you can tell them apart. Set the first one up completely before powering on the second, so you're always sure which unit you're talking to.

**Where is my information stored?**
Your settings and keys are stored on the Waypoint itself. It contacts the data providers to fetch departures, weather and so on.

---

## 11. Troubleshooting

**The display says "Waypoint first-time setup" and nothing changes**
Waypoint doesn't have your Wi-Fi details yet. Follow [section 3](#3-connect-to-wi-fi).

**The display says "Waypoint Setup – Complete setup in your browser"**
Wi-Fi is working but setup isn't finished. Open the address shown and finish the wizard. If you chose train times, it stays here until a Rail key has been saved.

**`waypoint.local` won't open**
Use the IP address shown on the display, and check that your phone or computer is on the same Wi-Fi network as Waypoint.

**"No services" or "No data available"**
Check that a station or stop is selected in its tab (pick from the drop-down list rather than just typing). For trains, check your Rail key. Then open **🖥 System** and look at **Last Result** for a clue.

**Trains show "Unauthorised"**
The Rail key is missing or wrong. Re-enter it under **⚙ Settings → API Keys** and reboot. Make sure you copied the **Consumer key**, not the secret, and that the feed type matches the key you have.

**Tube or bus shows no services**
TfL sometimes has maintenance windows, especially at weekends. Wait a few minutes. Adding a free TfL key helps.

**Weather isn't showing**
Weather needs an OpenWeatherMap key, and brand-new keys can take a couple of hours to start working.

**The touch button won't switch to Air or Space**
Check the mode is ticked under **⚙ Settings → Modes**; switched-off modes are skipped. Air and Space also need your location, which the wizard sets from your postcode.

**Something is still wrong**
Open **🖥 System** and note down the diagnostics (Wi-Fi signal, free memory, last result), then use **⟳ Reboot**. Rebooting fixes most one-off problems. If it keeps happening, get in touch (section 13).

---

## 12. Resetting your Waypoint

| Reset | How | What's erased |
|---|---|---|
| **Wi-Fi only** | Web page → **🖥 System → Erase WiFi** | Your Wi-Fi details only. Waypoint brings back its own network so you can join a new one. |
| **Ground settings** | **🖥 System → Clear Ground Mode Settings** | Your Rail, Bus, Tube and Combined stations |
| **Factory reset** | **🖥 System → Factory Reset** | Everything: settings, keys and Wi-Fi |
| **Factory reset using the touch button** | Unplug and replug the power, then **touch and hold the sensor during the start-up splash** (the first couple of seconds). A "Factory Reset" screen appears. Keep holding until the bar fills. | Everything: settings, keys and Wi-Fi |

<img width="1330" height="830" alt="factory reset" src="https://github.com/user-attachments/assets/5a6c2964-3ccc-403f-80ac-9218a11c1857" />

The touch-button reset is useful if you can't reach the web page. Let go before the bar fills to cancel.

---

## 13. Support

If you have any issues with your Waypoint at any time, or have an suggestions for potential improvement, do not hesitate to contact me directly via the means you purchased your Waypoint from.

If you need help, please include your **firmware version** (shown at the top of the Waypoint page, and on the System tab) and a description of what the display shows.

---

## Data sources

Waypoint uses data from National Rail / Rail Delivery Group, Transport for London, BusTimes, adsb.lol (with adsb.fi as a fallback), OpenWeatherMap, AeroDataBox and public satellite orbital data. Each is credited on the display when Waypoint starts, and each is subject to its own licence and terms.

https://github.com/user-attachments/assets/24549fa2-bc2c-4948-b061-1f4338408637
