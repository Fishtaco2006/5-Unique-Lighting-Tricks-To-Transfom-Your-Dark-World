# 5 Unique Lighting Tricks to Transform Your Dark World

Lighting isn’t just about seeing where you’re going — it sets the tone, guides the player, and makes your world feel alive. In this tutorial, we’ll start with a quick overview of the **Lighting Gizmo** and the **Environment Gizmo**, and then go through **five creative lighting techniques** you can use to elevate any dark environment.

---

## 🔧 Lighting Gizmo Overview

<img width="293" height="239" alt="image" src="https://github.com/user-attachments/assets/efa094f4-c01b-492b-ba26-56ce1d16c858" />

The **Lighting Gizmo** gives you full control over dynamic light sources in your world. It’s used to create spotlights, point lights, and other custom lighting effects.

<img width="299" height="436" alt="image" src="https://github.com/user-attachments/assets/345f56bd-ca04-44c1-a5e8-47f0a6d5fb66" />

You can configure:
- **Light Type** – Point, Spot, or Directional.
- **Intensity** – Brightness of the light.
- **Range** – How far the light reaches.
- **Color** – Use to match environment tone (e.g. warm for fire, cool for moonlight).
- **Shadows** – Enable realistic shadows.
- **Flicker** – Add motion or energy to the light (good for torches).

We'll use this gizmo in all five lighting effects below.

---

## 🌍 Environment Gizmo Overview

<img width="206" height="206" alt="image" src="https://github.com/user-attachments/assets/286b758a-0612-46e9-a8ee-cf0262b662c7" />

The **Environment Gizmo** lets you control the atmosphere of your world. It affects how your sky, fog, lighting, and ambient environment look and feel. This is especially important when creating darker or stylized environments.

<img width="298" height="314" alt="image" src="https://github.com/user-attachments/assets/11fe4ac8-6175-4879-8725-aa06809d8340" />

Here’s what each setting does:

### ✅ Active
- Turns the Environment Gizmo on/off.  
- Must be enabled for any other settings to apply.

### 🌌 Skydome Type
- Sets the type of sky used.
  - **Cubemap**: Realistic skybox textures (e.g. clouds, sunset).
  

### 🖼️ Texture
- Choose a specific sky texture when using **Cubemap** mode.  
- Options include Clear Day, Sunset, Overcast, etc.

### 🔄 Texture Rotation
- Rotates the sky dome around the Y-axis.
- Useful for positioning object in the sky.

### ☀️ Exposure
- Controls the overall brightness of the environment.
- Lower values = darker tone; higher = brighter scenes.

### 💡 Custom Light Intensity
- Allows manual control over light from the environment.

### 🔆 Light Intensity
- Works with the custom toggle to set how strong the sky lighting is.

### 🎨 Custom Fog Color
- Enables manual fog coloring instead of default values.

### 🌫️ Fog Color
- Define the RGB color of your fog.
- Example: Orange fog = `1, 0.41, 0`.

### 🌁 Fog Density
- Controls how thick the fog appears.
- Adds mood, depth, or mystery.

### 🧱 Show Grid
- Shows a grid in the editor view. Helps with object placement.

### 🎙️ VOIP Settings
- Controls voice chat behavior in this zone.

> Pro Tip: Use fog + exposure creatively to simulate night, magic zones, or storms. Always test visibility from a player’s perspective!

---

## 1. 🐞 Fireflies
<img width="1366" height="528" alt="image" src="https://github.com/user-attachments/assets/d5f9ec20-a330-482b-91b6-ac867183c091" />

Create tiny glowing orbs that float gently in the air.

**What it does:**  
Adds ambient, magical lighting that moves and sparkles.

**How to make it:**
- Click on the cube on the top left corner of the editor, then click on ***Empty Object*** in the drop down menu to spawn an Empty Object.
  <img width="1357" height="666" alt="image" src="https://github.com/user-attachments/assets/9a978f28-623e-42a0-9a74-07774505c02d" />




- Go to ***public assets***, change the search category to ***VFX***, the scroll down to find the ***Imapct A*** effect, and drag it on the screen.
  <img width="1358" height="619" alt="image" src="https://github.com/user-attachments/assets/11239d3f-5ebc-4de5-9ec6-a8354f80430e" />

- Change the VFX name to Sparkle
- Change the ***Prefab Name*** to ***impact_style_a***
- Turn on ***Looping***, change ***SparkleID (0-15)*** to ***5***
- Change ***SparkleRotation*** to ***30, -30***.
- Change ***SparkleScale*** to ***0***.
- Change ***SparkleColorHSVA*** to ***0, 0, 1, 1***.(Change to your desired color here)
- Change ***SparkleLifetime*** to ***1, 0.5***.
- Turn on ***GlowToggle***.
- Change ***GlowLifetime*** to ***1, 0.4***.
- Change ***GlowColor*** to ***0, 0, 1, 1***. (Change to your desired color here)
- Turn off ***TinySparkleToggle***. ( Values of next 5 variables irrelevant)
- Turn on ***RingToggle***.
- Change ***RingScale*** to ***0.1***.
- Change ***RingColorHSVA*** to ***0, 0, 1, 1***. (Change to your desired color here)
- Change ***RingLifeTime*** to ***0.1, 0.4***.
- Change ***GlobalScale*** to ***1***.
  <img width="1363" height="550" alt="image" src="https://github.com/user-attachments/assets/2aa35fed-b82c-4629-a2ab-babf550038ea" />

  <img width="1363" height="529" alt="image" src="https://github.com/user-attachments/assets/5b58e19f-a204-47d3-8523-e1140ce733ef" />

- Next, add a ***Dynamic Light***.
- Turn on ***Enabled***.
- Change ***Light Type*** to ***Point***
- Change ***Color*** to ***1, 1, 1 (White)***. (Change to your desired color here)
- Change ***Intensity*** to ***0.5***.
- Change ***Falloff Distance** to ***1***.

  <img width="1363" height="551" alt="image" src="https://github.com/user-attachments/assets/17525303-5c8a-4ae1-8260-1e4ad5d71fc6" />

- Make sure the ***Dynamic Light*** and the ***Sparkle VFX*** are centered
  
  <img width="347" height="189" alt="image" src="https://github.com/user-attachments/assets/e3149255-03b2-4497-afaf-0a62833b15c5" /> <img width="195" height="189" alt="image" src="https://github.com/user-attachments/assets/a7a2f6ad-9bd4-4324-b120-8b5cd76de154" />



- Drag the ***Dynamic Light*** and the ***Sparkle VFX*** into the empty object and rename the empty object to ***FireFly***
  
  <img width="306" height="147" alt="image" src="https://github.com/user-attachments/assets/81a9c6f3-3cf8-41c0-8ba8-69140ac54718" />

  
- Make a script called ***FireFly_Logic***, add the code below to the script, save the script, and add the script to the fire fly object
  
  <img width="416" height="189" alt="image" src="https://github.com/user-attachments/assets/fbd74375-e900-44ae-b310-acbc044ce5bc" />





**Bonus:** Use soft colors like pale blue or gold for mood.

---

## 2. 🔦 Rotating Spotlight (Searchlight)

Simulates a guard tower or sci-fi beacon sweeping the area.

**What it does:**  
Adds directional lighting and creates tension or focus.

**How to use it:**
- Use a **Spot Light** with narrow angle and long range.
- Attach it to a rotating object or use a script.
- Sweep back and forth with animation or sin curve logic.

**Best used in:** Bases, prisons, stormy outposts.

---

## 3. 🧚 Fairy Companion Light

Make a glowing orb that follows the player and lights their path.

**What it does:**  
Adds mobile lighting and a magical companion feel.

**How to use it:**
- Create a small object with a **Point Light**.
- Attach a script to follow the player at a short offset.
- Optionally add flicker, glow, or wing particles.

**Perfect for:** Fantasy, story-driven, or moody worlds.

---

## 4. 🔥 Flickering Torches and Lanterns

Use flickering to make static lights feel warm and alive.

**What it does:**  
Simulates fire or candlelight in dark areas.

**How to use it:**
- Use a **Point Light** with orange/yellow color.
- Enable **Flicker** and adjust intensity variation.
- Attach to torches, lanterns, sconces.

**Add ons:** Fire sound, smoke particles, shadows.

---

## 5. ✨ Neon Signs

Glow up your dark city or interior scenes with vibrant signage.

**What it does:**  
Creates eye-catching focal points and improves visibility.

**How to use it:**
- Use mesh text or emissive planes.
- Place **Point Lights** or **Area Lights** near the sign.
- Match the light color to the sign’s theme.
- Use bold colors like neon blue, magenta, green.

**Great for:** Cyberpunk cities, shops, arcades, or fun themed worlds.

---

## 🎯 Final Tips

- Use a mix of static and animated lights.
- Combine Environment + Lighting Gizmo settings for deeper control.
- Keep some areas darker to let your light effects shine.
- Let lighting guide the player emotionally and physically.

---

## ✨ Conclusion

With just a few simple techniques, you can take a dark, empty-feeling world and make it come to life with color, movement, and atmosphere. Whether you’re creating fantasy forests, dungeons, neon-lit cities, or haunted caves — these lighting tricks give you the tools to transform your world.

Make your lights **tell a story**.
