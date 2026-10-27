# Waypoint Guide

![Waypoint on a desk showing live departures](images/01-hero.png)

Waypoint is a live departures board for your desk, shelf or wall. It shows real-time **trains, buses and Tube services**, the **aircraft flying overhead**, and **satellites passing over your home**, all on a crisp OLED display.

This guide takes you from the box to a working board in about ten minutes.

## Quick start

1. **Plug it in** to a USB power supply.
2. **Join the "Waypoint" Wi-Fi network** on your phone and tell the board your home Wi-Fi details.
3. **Open the setup page** in your browser and run the **Setup Wizard** with your postcode.
4. *(Train times only)* Paste in a free Rail Data Marketplace key.
5. Done. Use the **touch button** to flip between stations and modes.

The rest of this guide walks through each step with pictures.

---

## Contents

1. [What you need](#1-what-you-need)
2. [Plug in your Waypoint](#2-plug-in-your-waypoint)
3. [Connect to Wi-Fi](#3-connect-to-wi-fi)
4. [Open the setup page](#4-open-the-setup-page)
5. [Run the Setup Wizard](#5-run-the-setup-wizard)
6. [Get a Rail key (train times only)](#6-get-a-rail-key-train-times-only)
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
- A USB power supply and cable <!-- TODO: confirm what is supplied in the box and the connector type -->
- A **2.4 GHz Wi-Fi network** and its password. Waypoint can't use 5 GHz-only networks. Most home routers broadcast both, so you don't normally need to do anything.
- A phone, tablet or computer on the same Wi-Fi network

![The back of the unit, showing the power connection and the touch sensor](images/02-unit-overview.png)

Train times need one free key (see [section 6](#6-get-a-rail-key-train-times-only)). Buses, Tube, aircraft and satellites need no keys at all.

---

## 2. Plug in your Waypoint

Connect the power. After a moment the display lights up with a short animated splash.

![Start-up splash screen](images/03-boot-splash.png)

> **Tip:** try not to touch the touch sensor during the first couple of seconds after power-up. Touching it during the splash starts the factory-reset countdown (see [section 12](#12-resetting-your-waypoint)). Letting go straight away cancels it.

---

## 3. Connect to Wi-Fi

A brand-new Waypoint doesn't know your Wi-Fi yet, so it creates a little Wi-Fi network of its own that you use to tell it.

**1.** After the splash, the display shows **"Waypoint first-time setup"**:

![Waypoint first-time setup screen](images/04-wifi-setup-screen.png)

**2.** On your phone, open **Wi-Fi settings** and join the network called **Waypoint**. There's no password.

![Joining the Waypoint network on a phone](images/05-phone-wifi-list.png)

**3.** A setup page should open by itself. If it doesn't, open a web browser and go to **http://192.168.4.1**.

![The Wi-Fi setup page menu](images/06-wifi-portal-menu.png)

**4.** Tap **Configure WiFi**, choose your home network from the list and type its password. Then tap **Save**.

![Choosing your home Wi-Fi network](images/07-wifi-portal-networks.png)

**5.** Waypoint connects to your network. When it works, the display shows **"Wi-Fi Connected"** along with the board's **IP address** in the corner. Make a note of it; you may need it in the next step.

![Wi-Fi Connected with the IP address](images/08-wifi-connected.png)

If the password is wrong, or the network is out of range, Waypoint goes back to its own **Waypoint** network so you can try again.

---

## 4. Open the setup page

Now that Waypoint is on your home network, make sure your phone or computer is on the **same network** and open a browser.

Type **http://waypoint.local** and press Go.

If that doesn't load (some phones and routers don't support `.local` addresses), type the **IP address from the display** instead, for example `http://192.168.1.50`.

The display now shows **"Waypoint Setup – Complete setup in your browser"**, with the address to use:

![Display asking you to complete setup in your browser](images/09-oled-complete-setup.png)

The page automatically opens the **Setup Wizard**.

---

## 5. Run the Setup Wizard

The wizard has four steps and sets up all of Waypoint's modes in one go. You can rerun it whenever you like using the **🧭 Setup Wizard** button at the top of the page.

### Step 1: Location

Type your **postcode** and tap **Find Stops**. Waypoint uses it to find your nearest stations and stops, to centre the aircraft and satellite tracking on your home, and for local weather.

![Wizard step 1](images/10-wizard-step1.png)

### Step 2: Confirm and configure

Check the suggestions and change anything that isn't right.

![Wizard step 2](images/11-wizard-step2.png)

- **Nearest train station**: pick one.
- **Nearest Tube / DLR / Elizabeth line station**: pick one, or **Skip** if you don't use them.
- **Nearest bus stop**: pick one, or **Skip**.
- **Air mode**: the search radius is how far from home to look for aircraft (default 20 nautical miles).
- **Space mode**: choose which satellites to look for (space stations, Starlink, weather satellites and more).
- **Weather**: switch on to show the temperature and conditions. This needs a free OpenWeatherMap key (next step).
- **Hostname**: the name in `waypoint.local`. Leave it as it is unless you have more than one Waypoint.
- **Flip Display**: turn this on if the unit sits upside-down.
- **Sleep Mode**: blanks the display overnight between the hours you choose.
- **Firmware updates**: leave both ticked and Waypoint keeps itself up to date.

### Step 3: API keys

![Wizard step 3](images/12-wizard-step3.png)

Only **train times** need a key. Everything else here is optional, so you can leave the fields blank and add keys later.

| Key | Needed for |
|---|---|
| **Rail Data Marketplace key** | Train departures ([how to get one](#6-get-a-rail-key-train-times-only)) |
| **OpenWeatherMap key** | Weather display |
| **TfL key** | Optional. Reduces the chance of Tube and bus lookups being rate-limited. |
| **RapidAPI key** | Optional. Only for Flight Watch scheduled times. |

### Step 4: Default mode

![Wizard step 4](images/13-wizard-step4.png)

- **Modes This Board Uses**: untick anything you don't want. The touch button will skip those modes.
- **Default board mode**: Ground (trains, buses, Tube), Air (planes) or Space (satellites). This is what Waypoint starts in.
- **Ground sub-mode**: if you chose Ground, pick Rail, Tube, Bus or Combined. *Combined* mixes all three into one board, sorted by time.

Tap **Apply Everything to Board**. Your first departures will appear on the display shortly after.

> Each mode can hold up to **four** stations or stops. The wizard sets up the first one. You can add more later (see [section 8](#8-changing-things-later)) and flip between them with a tap.

---

## 6. Get a Rail key (train times only)

National Rail data is free, but the Rail Delivery Group asks everyone to register for a key. It takes about five minutes.

1. Go to [raildata.org.uk](https://raildata.org.uk) and create a free account.
2. Open the **Data Product Catalogue** and search for **LDBWS**.
3. Choose **Live Departure Board (Public)** and **subscribe**, accepting the licence.
4. Go to **My Subscriptions** and open the **Specification** tab.
5. Copy the **Consumer key**. (Not the *secret*.)
6. Back on your Waypoint page, paste it into the **Rail Data Marketplace key** box and save.

Until Waypoint has a key, it stays on the setup screen if it's set to show trains. Once you save it, it restarts by itself.

> If you already have an older National Rail "Darwin" token, you can use it by choosing **Legacy OpenLDBWS** as the feed. New tokens are no longer issued, so most people should use the Rail Data Marketplace key.

### Optional keys

**OpenWeatherMap (weather):** sign up at [openweathermap.org](https://home.openweathermap.org/users/sign_up), confirm your email, open the **API keys** tab and copy the default key. New keys can take up to a couple of hours to start working.

**TfL (Tube and bus, optional):** register at the [TfL API portal](https://api-portal.tfl.gov.uk/signup), open **Products**, subscribe to **500 Requests per min**, then copy your key from **Profile → Show key**.

**RapidAPI / AeroDataBox (Flight Watch, optional):** sign up at [rapidapi.com](https://rapidapi.com), subscribe to the free **Basic** plan on the **AeroDataBox** API page, and copy the **X-RapidAPI-Key** from any sample code snippet.

---

## 7. Using the touch button

Waypoint has no screen buttons. Instead, there is a **touch sensor** you just tap or hold with a finger.

![Finger on the touch sensor](images/14-touch-sensor.png)

- **Tap**: touch and let go quickly.
- **Hold**: keep your finger on it for about half a second or more.
- When Waypoint asks you to **hold to confirm**, a progress bar appears. Keep holding until it fills, or let go to cancel.

### Trains, buses and Tube

| Do this | And this happens |
|---|---|
| **Tap** | Show the next station or stop you've set up. A banner shows which one (for example *Slot 2/3*). |
| **Hold** | Switch between **Rail → Bus → Tube → Combined**. |
| **Keep holding** | A **"Switch to Air Mode"** prompt appears. Keep holding to confirm, or let go to stay put. |

![Slot banner](images/15-slot-banner.png)

![Switch to Air Mode prompt with progress bar](images/16-mode-switch-prompt.png)

### Aircraft (Air mode)

| Do this | And this happens |
|---|---|
| **Tap** | Flip through the details of each plane overhead, and back to the list. |
| **Hold** | "Switch to Space Mode" prompt. Keep holding to confirm. |

If you're tracking a specific flight with **Flight Watch**, a tap switches between the progress bar and the live panel, and a hold lets you cancel tracking.

### Satellites (Space mode)

| Do this | And this happens |
|---|---|
| **Tap** | Flip through the satellites overhead, and back to the list. |
| **Hold** | "Switch to Ground Mode" prompt. Keep holding to confirm. |

The hold cycle goes **Ground → Air → Space → Ground**. Any mode you've turned off is skipped.

You can also switch modes from the **Ground / Air / Space** tabs at the top of the Waypoint web page.

---

## 8. Changing things later

Open **http://waypoint.local** (or the IP address) any time to change settings.

![The Waypoint page](images/17-dashboard.png)

- **Rail, Bus, Tube, Combined tabs**: add more stations and stops (up to four each), filter by platform, route or line, or add a walking-time offset so you only see trains you can still catch.
- **⚙ Settings**: brightness, sleep hours, flip display, weather, hostname, timezone outside the UK, which modes to use and API keys. Tap **💾 Save Settings** when you're done.
- **🖥 System**: reboot, check for updates, back up or restore your settings, and see how well Waypoint is running.

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
Air and Space modes work anywhere. Trains, buses and the Tube use UK data. Set your timezone under Settings if you're outside the UK.

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

![Factory reset screen](images/18-factory-reset-screen.png)

The touch-button reset is useful if you can't reach the web page. Let go before the bar fills to cancel.

---

## 13. Support

<!-- TODO: add support contact details, returns/warranty information and any order-number instructions. -->

If you need help, please include your **firmware version** (shown at the top of the Waypoint page, and on the System tab) and a description of what the display shows.

---

## Data sources

Waypoint uses data from National Rail / Rail Delivery Group, Transport for London, BusTimes, adsb.lol (with adsb.fi as a fallback), OpenWeatherMap, AeroDataBox and public satellite orbital data. Each is credited on the display when Waypoint starts, and each is subject to its own licence and terms.
