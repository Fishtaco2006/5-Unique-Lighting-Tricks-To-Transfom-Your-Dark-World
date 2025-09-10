# 5 Unique Lighting Tricks to Transform Your Dark World

Lighting isn’t just about seeing where you’re going — it sets the tone, guides the player, and makes your world feel alive. In this tutorial, we’ll start with a quick overview of the **Lighting Gizmo** and the **Environment Gizmo**, and then go through **five creative lighting techniques** you can use to elevate any dark environment.

---

## 🔧 Lighting Gizmo Overview

<img width="293" height="239" alt="image" src="https://github.com/user-attachments/assets/efa094f4-c01b-492b-ba26-56ce1d16c858" />

The **Lighting Gizmo** gives you full control over dynamic light sources in your world. It’s used to create spotlights, point lights, and other custom lighting effects.

<img width="299" height="436" alt="image" src="https://github.com/user-attachments/assets/345f56bd-ca04-44c1-a5e8-47f0a6d5fb66" />

You can configure:
### 🔦 **Light Type**
- **Point**: Emits light in all directions from a central point (like a bulb or firefly).
- **Spot**: Emits light in a cone shape (like a flashlight or searchlight).


### 🎨 **Color (R, G, B)**
- The color of the light being emitted.
- Use warm colors (like 1, 0.6, 0.3) for firelight, or bright colors (like 0, 1, 0) for neon or energy.

### 💡 **Intensity**
- Controls how **bright** the light is.


### 📏 **Falloff Distance**
- Determines how far the light reaches before it fades out.
- Higher values = larger area affected.
- Lower values = tighter, more focused lighting.

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
![Fireflies Preview](https://github.com/user-attachments/assets/d5f9ec20-a330-482b-91b6-ac867183c091)

Create tiny glowing orbs that float gently in the air.

**What it does:**  
Adds ambient, magical lighting that moves and sparkles.

---

### 🔧 How to Make It

- Click on the cube in the top-left corner of the editor, then click on **_Empty Object_** in the drop-down menu.  
  ![Empty Object](https://github.com/user-attachments/assets/9a978f28-623e-42a0-9a74-07774505c02d)

- Go to **_Public Assets_**, change the search category to **_VFX_**, scroll down to find **_Impact A_**, and drag it onto the screen.  
  ![Impact A](https://github.com/user-attachments/assets/11239d3f-5ebc-4de5-9ec6-a8354f80430e)

#### 🎨 VFX Settings

- Rename VFX to `Sparkle`
- Set **Prefab Name** to `impact_style_a`
- Enable **Looping**
- Set **SparkleID (0–15)** to `5`
- Set **SparkleRotation** to `30, -30`
- Set **SparkleScale** to `0`
- Set **SparkleColorHSVA** to `0, 0, 1, 1`
- Set **SparkleLifetime** to `1, 0.5`
- Enable **GlowToggle**
- Set **GlowLifetime** to `1, 0.4`
- Set **GlowColor** to `0, 0, 1, 1`
- Disable **TinySparkleToggle**
- Enable **RingToggle**
- Set **RingScale** to `0.1`
- Set **RingColorHSVA** to `0, 0, 1, 1`
- Set **RingLifetime** to `0.1, 0.4`
- Set **GlobalScale** to `1`

![VFX Setup 1](https://github.com/user-attachments/assets/2aa35fed-b82c-4629-a2ab-babf550038ea)  
![VFX Setup 2](https://github.com/user-attachments/assets/5b58e19f-a204-47d3-8523-e1140ce733ef)

---

### 💡 Add a Dynamic Light

- Add a **Dynamic Light**
- Enable it
- Set **Light Type** to `Point`
- Set **Color** to `1, 1, 1`
- Set **Intensity** to `0.5`
- Set **Falloff Distance** to `1`

![Dynamic Light](https://github.com/user-attachments/assets/17525303-5c8a-4ae1-8260-1e4ad5d71fc6)

Center all components:  
![Centering 1](https://github.com/user-attachments/assets/41547660-b03c-4cde-b4fb-13399d86d4d6)  
![Centering 2](https://github.com/user-attachments/assets/a7a2f6ad-9bd4-4324-b120-8b5cd76de154)

---

### 🗃️ Organize Your Object

- Group the **Dynamic Light** and **Sparkle VFX** inside the Empty Object
- Rename the Empty Object to `FireFly`

![Grouping](https://github.com/user-attachments/assets/81a9c6f3-3cf8-41c0-8ba8-69140ac54718)

---

### 🧠 Firefly Logic Script

- Create a script called `FireFly_Logic`, paste the following code, and attach it to the `FireFly` object  
  ![Script Attachment](https://github.com/user-attachments/assets/fbd74375-e900-44ae-b310-acbc044ce5bc)

```ts
import * as hz from 'horizon/core';

class Firefly extends hz.Component<typeof Firefly> {
  static propsDefinition = {
    minX: { type: hz.PropTypes.Number, default: -20 },
    maxX: { type: hz.PropTypes.Number, default: 20 },
    minY: { type: hz.PropTypes.Number, default: 5 },
    maxY: { type: hz.PropTypes.Number, default: 10 },
    minZ: { type: hz.PropTypes.Number, default: -20 },
    maxZ: { type: hz.PropTypes.Number, default: 20 },
    speed: { type: hz.PropTypes.Number, default: 1 },
  };

  private direction!: hz.Vec3;
  private timer!: number;

  start() {
    this.direction = this.getRandomDirection();
    this.timer = this.async.setInterval(() => {
      this.direction = this.getRandomDirection();
    }, 5000);
    this.connectLocalBroadcastEvent(hz.World.onUpdate, this.update.bind(this));
  }

  getRandomDirection(): hz.Vec3 {
    const angleXZ = Math.random() * 2 * Math.PI;
    const angleY = (Math.random() - 0.5) * Math.PI;
    return new hz.Vec3(
      Math.cos(angleXZ) * Math.cos(angleY),
      Math.sin(angleY),
      Math.sin(angleXZ) * Math.cos(angleY)
    );
  }

  update(data: { deltaTime: number }) {
    const position = this.entity.position.get();
    const newPosition = position.add(this.direction.mul(this.props.speed! * data.deltaTime));

    if (newPosition.x < this.props.minX! || newPosition.x > this.props.maxX!) this.direction.x *= -1;
    if (newPosition.y < this.props.minY! || newPosition.y > this.props.maxY!) this.direction.y *= -1;
    if (newPosition.z < this.props.minZ! || newPosition.z > this.props.maxZ!) this.direction.z *= -1;

    this.entity.position.set(newPosition);
  }

  dispose() {
    this.async.clearInterval(this.timer);
  }
}

hz.Component.register(Firefly);
```

**Settings Explanation:**

| Property | Description |
|----------|-------------|
| `minX`, `maxX` | X-axis boundaries |
| `minY`, `maxY` | Y-axis boundaries |
| `minZ`, `maxZ` | Z-axis boundaries |
| `speed` | Movement speed |

![Script Variables](https://github.com/user-attachments/assets/3070b4d7-d6b0-438b-9ab2-1a39d461a2fe)

---

### 📂 Save as Asset

- Right-click the `FireFly` object > **Create Asset**  
  ![Create Asset](https://github.com/user-attachments/assets/2f2941e4-3099-407d-a410-8d1d61719604)
- Name it `Firefly` and click **Create**  
  ![Save Asset](https://github.com/user-attachments/assets/838bc3fb-1c98-4b70-b2c2-421bce33c642)

---

## ♻️ Firefly Spawner

- Create an **Empty Object**, name it `FireFly Spawner`, and add a script called `FireFly_Spawner`  
  ![Spawner Setup](https://github.com/user-attachments/assets/39e012c9-d077-4a57-9a2b-eb2041c81fd6)  
  ![Spawner Script](https://github.com/user-attachments/assets/180c07db-de94-41c4-822f-46e0772e8058)

```ts
import { Asset, Entity } from 'horizon/core';
import * as hz from 'horizon/core';

class FireflySpawner extends hz.Component<typeof FireflySpawner> {
  static propsDefinition = {
    fireflyAsset: { type: hz.PropTypes.Asset },
    spawnLocation: { type: hz.PropTypes.Entity },
    maxFireflies: { type: hz.PropTypes.Number, default: 10 },
  };

  private fireflies: Entity[] = [];

  private spawnFirefly(): void {
    if (this.props.fireflyAsset! && this.props.spawnLocation! && this.fireflies.length < this.props.maxFireflies!) {
      const spawnPosition = this.props.spawnLocation!.position.get();
      this.world.spawnAsset(this.props.fireflyAsset!, spawnPosition).then((entities) => {
        const firefly = entities[0];
        this.fireflies.push(firefly);
      });
    } else if (this.fireflies.length >= this.props.maxFireflies!) {
      const oldestFirefly = this.fireflies.shift();
      if (oldestFirefly) {
        this.world.deleteAsset(oldestFirefly, true);
        this.spawnFirefly();
      }
    }
  }

  start(): void {
    this.async.setInterval(() => {
      this.spawnFirefly();
    }, 2000);
  }

  dispose(): void {
    this.fireflies.forEach((firefly) => {
      this.world.deleteAsset(firefly, true);
    });
    this.fireflies = [];
  }
}

hz.Component.register(FireflySpawner);
```

- Attach the script to `FireFly Spawner`  
- Assign the `fireflyAsset`, `spawnLocation`, and `maxFireflies` values  
  ![Spawner Settings](https://github.com/user-attachments/assets/a2302bf4-6489-45c6-851c-6ce6fc0bcf02)

---

## 📊 Testing

- Add an **Environment Gizmo** and set the cubemap to `Midnight Black`  
  ![Environment](https://github.com/user-attachments/assets/8bdf089b-b1bd-4987-a901-0aad84997627)

- Preview the world  
  ![Preview](https://github.com/user-attachments/assets/c9bd0ae3-8a9b-473f-897a-631524794ad0)  
  ![Forest](https://github.com/user-attachments/assets/d5f9ec20-a330-482b-91b6-ac867183c091)

---

## ⚠️ Performance Tip

Dynamic lights are **performance heavy**. If enabled, you can only spawn ~15 fireflies. Without them, you can spawn many more.

**With Dynamic Lighting**  
![With Light](https://github.com/user-attachments/assets/d5f9ec20-a330-482b-91b6-ac867183c091)

**Without Dynamic Lighting**  
![Without Light](https://github.com/user-attachments/assets/cceb99d2-b78c-40ad-ad3d-bbe00f31b766)

---

## 2. 🔦 Rotating Spotlight (Searchlight)

Simulates a guard tower or sci-fi beacon sweeping the area.

**What it does:**  
Adds directional lighting and creates tension or focus.

**How to use it:**
- Go to Public Assets, search for a ***search light***, drag it into the world and rename it Search Light.
  
  <img width="1054" height="614" alt="image" src="https://github.com/user-attachments/assets/5b7326c8-6fb3-474c-82c3-f2c3db1c2944" />

<img width="292" height="481" alt="image" src="https://github.com/user-attachments/assets/b29a3c71-97f6-497f-814c-c2d137d64ea5" />


- Click on the cube on the top left corner and in the drop down menu click on shapes, then drag the object named ***Cylinder C*** into the world.

<img width="833" height="614" alt="image" src="https://github.com/user-attachments/assets/03363c6b-8937-4ed9-95bc-c47b964888f6" />


  <img width="992" height="564" alt="image" src="https://github.com/user-attachments/assets/14ceb2d6-18c5-43db-b13e-7c5889a7d736" />

- Change the name of the cylinder to led and then change the properties of the cylinder to those seen in the image below:

  <img width="300" height="514" alt="image" src="https://github.com/user-attachments/assets/f225332e-81d5-401a-8cfc-06b33af5a309" />

- Drag the ***LED Object*** and center it to the lens of the ***Search Light***.
  
  <img width="424" height="246" alt="image" src="https://github.com/user-attachments/assets/1c0a8e73-c3fe-48c0-8d0f-f1ccd5bd6b3e" /> <img width="325" height="253" alt="image" src="https://github.com/user-attachments/assets/ba5a4b20-8f9a-4234-9f85-d3ade1ab394c" />

- Go to Gizmos and drag a dynamic light into the scene.

<img width="718" height="441" alt="image" src="https://github.com/user-attachments/assets/c7f4295d-889b-4307-a8b7-3ecb1f53007b" />

<img width="780" height="555" alt="image" src="https://github.com/user-attachments/assets/5712db52-5b6f-40ca-8066-86161d6fb256" />

- Center the Dynamic Light to the ***LED Object*** and the ***Search Light***.

  <img width="1064" height="518" alt="image" src="https://github.com/user-attachments/assets/cb68d4d8-f8c0-407c-91fc-582b26c1e23a" />

<img width="1057" height="493" alt="image" src="https://github.com/user-attachments/assets/4947534c-d142-4156-ab85-b93dbd2a4a49" />

- Click on the cube at the top left, then click on sounds and search for ***Mechanical Alarm Triple (Random)***, then drag the sound into the scene.

<img width="355" height="359" alt="image" src="https://github.com/user-attachments/assets/fa7e08ce-80f6-410d-a46a-84331f760a47" />

<img width="698" height="510" alt="image" src="https://github.com/user-attachments/assets/62aac9cb-844e-4368-ac18-22e6b29c97d2" />

- Center the Alarm Sound with the rest.

  <img width="472" height="266" alt="image" src="https://github.com/user-attachments/assets/2c979152-c2fc-45e2-b087-78c82989bc01" />

<img width="279" height="231" alt="image" src="https://github.com/user-attachments/assets/1975eda0-6977-4836-bfba-c6013055829d" />


-Drag the Dynamic Light, Alarm Sound and LED object into the Search Light.

<img width="1019" height="385" alt="image" src="https://github.com/user-attachments/assets/ef0822de-3bb0-4035-9c51-a9cde9a37afa" />

- Drag a trigger into the scene called ***Search Light Range***, position it just in front of the searchlight,and then drag it into the search light object (this is how the search light finds players).

**Note:** You can adjust the size of the trigger for your use case

  <img width="1366" height="491" alt="image" src="https://github.com/user-attachments/assets/d42c6bca-1492-4641-ac7d-6fa1306e0170" />


- Now, drag an environent gizmo into the scene and set the Texture to ***Midnight Black***.
  
  <img width="1056" height="551" alt="image" src="https://github.com/user-attachments/assets/02b6696b-e976-4fff-8c14-0528293ecb1c" />

- Now, the search light is coming together. Next we need the script.

  <img width="905" height="408" alt="image" src="https://github.com/user-attachments/assets/f68be323-15c3-4d38-b81a-400f13afa985" />


- Now, make a new script called ***Search_Light_Logic*** and copy the code below into it.

<img width="516" height="551" alt="image" src="https://github.com/user-attachments/assets/f571d7f1-9951-46e5-ae68-9fde17063c70" />

  ***Search_Light_Logic:***

```typescript

  import { Entity } from 'horizon/core';
import * as hz from 'horizon/core';

class Searchlight extends hz.Component<typeof Searchlight> {
  static propsDefinition = {
    trigger: { type: hz.PropTypes.Entity },
    led: { type: hz.PropTypes.Entity },
    light: { type: hz.PropTypes.Entity },
    alarmSound: { type: hz.PropTypes.Entity },
    scanAngle: { type: hz.PropTypes.Number, default: 30 },
    scanSpeed: { type: hz.PropTypes.Number, default: 1 },
    tiltAngle: { type: hz.PropTypes.Number, default: 30 }, // New property for tilt angle
    offset: { type: hz.PropTypes.Number, default: 90 }, // New property for offset angle
  };

  private trackedPlayer: hz.Player | null = null;
  private scanDirection: number = 1;
  private alarmTimer: number = 0;
  private initialRotation!: hz.Quaternion;

  preStart() {
    this.connectCodeBlockEvent(this.props.trigger!, hz.CodeBlockEvents.OnPlayerEnterTrigger, this.onPlayerEnter.bind(this));
    this.connectCodeBlockEvent(this.props.trigger!, hz.CodeBlockEvents.OnPlayerExitTrigger, this.onPlayerExit.bind(this));
    this.connectLocalBroadcastEvent(hz.World.onUpdate, this.update.bind(this));
  }

  start() {
    // Initialize the LED and light colors to white
    this.props.led!.as(hz.MeshEntity).style.tintColor.set(hz.Color.white);
    this.props.light!.as(hz.DynamicLightGizmo).color.set(hz.Color.white);
    this.initialRotation = this.entity.rotation.get();
  }

  onPlayerEnter(player: hz.Player) {
    this.trackedPlayer = player;
    // Change the LED and light colors to red
    this.props.led!.as(hz.MeshEntity).style.tintColor.set(hz.Color.red);
    this.props.light!.as(hz.DynamicLightGizmo).color.set(hz.Color.red);
    this.props.alarmSound!.as(hz.AudioGizmo).play();
  }

  onPlayerExit(player: hz.Player) {
    if (this.trackedPlayer === player) {
      this.trackedPlayer = null;
      // Change the LED and light colors back to white
      this.props.led!.as(hz.MeshEntity).style.tintColor.set(hz.Color.white);
      this.props.light!.as(hz.DynamicLightGizmo).color.set(hz.Color.white);
    }
  }

  update(data: { deltaTime: number }) {
    if (this.trackedPlayer) {
      // Make the searchlight look at the tracked player
      const direction = hz.Vec3.sub(this.trackedPlayer.position.get(), this.entity.position.get()).normalize();
      const rotation = hz.Quaternion.lookRotation(direction);
      // Apply tilt angle
      const tiltRotation = hz.Quaternion.fromAxisAngle(hz.Vec3.forward, hz.degreesToRadians(this.props.tiltAngle!));
      
      const additionalRotation = hz.Quaternion.fromAxisAngle(hz.Vec3.up, hz.degreesToRadians(this.props.offset));
      this.entity.rotation.set(additionalRotation.mul(rotation).mul(tiltRotation));
      
      // Play alarm sound every 3 seconds
      this.alarmTimer += data.deltaTime;
      if (this.alarmTimer >= 3) {
        this.props.alarmSound!.as(hz.AudioGizmo).play();
        this.alarmTimer = 0;
      }
    } else {
      // Scan the area
      const currentRotation = this.entity.rotation.get();
      const targetRotation = hz.Quaternion.fromAxisAngle(hz.Vec3.up, hz.degreesToRadians(this.scanDirection * this.props.scanAngle!)).mul(this.initialRotation);
      // Apply tilt angle to target rotation
      const tiltRotation = hz.Quaternion.fromAxisAngle(hz.Vec3.forward, hz.degreesToRadians(-this.props.tiltAngle!));
      const tiltedTargetRotation = tiltRotation.mul(targetRotation);
      const newRotation = hz.Quaternion.slerp(currentRotation, tiltedTargetRotation, data.deltaTime * this.props.scanSpeed!);
      this.entity.rotation.set(newRotation);

      // Update scan direction
      const angleBetweenQuaternions = (q1: hz.Quaternion, q2: hz.Quaternion) => {
        const dot = Math.abs(q1.x * q2.x + q1.y * q2.y + q1.z * q2.z + q1.w * q2.w);
        return Math.acos(Math.min(dot, 1)) * 2;
      };
      const angle = angleBetweenQuaternions(currentRotation, tiltedTargetRotation);
      if (Math.abs(hz.radiansToDegrees(angle)) < 1) {
        this.scanDirection *= -1;
      }
    }
  }
}

hz.Component.register(Searchlight);

```

- Attach this script to the search light and edit the variables as such:

  <img width="297" height="264" alt="image" src="https://github.com/user-attachments/assets/42c648a2-79a0-481c-9b34-f66d7968371e" />

- To explain what these variables do

  ## 🔦 Search Light Logic Properties

The `Search_Light_Logic` component controls a dynamic rotating spotlight that can detect players, play alarms, and simulate patrol behavior. Here's what each property does:

| **Property**     | **Type**         | **Description** |
|------------------|------------------|------------------|
| `trigger`        | Entity Reference | The detection trigger zone (e.g., sphere or box collider) that activates the searchlight when something enters. |
| `led`            | Entity Reference | A visual object like an LED or spotlight mesh that rotates along with the light. |
| `light`          | Dynamic Light    | The actual dynamic light component that emits visible light into the scene. |
| `alarmSound`     | Sound Asset      | A sound that plays when the trigger is activated — typically a siren or alarm. |
| `scanAngle`      | Number (degrees) | How far the searchlight rotates left and right from its center. A value of `30` rotates from -30° to +30°. |
| `scanSpeed`      | Number           | How fast the light moves while scanning. Higher values mean faster sweeping. |
| `tiltAngle`      | Number (degrees) | The vertical angle the light is tilted. Useful for aiming the light downward or upward. |
| `offset`         | Number (degrees) | A rotational offset applied to the base direction of the light to align it correctly in your scene. |

***Note:*** The offset is there because of the search lights unique shape. The side of the search light would be pointing towards you instead front. If you are using it for another assets and the orientation is off. Try changing the value of the offset by 90 degrees until it looks right.



- This script makes it so that the search light patrols the area until a player enters the trigger when the player enters, it locks onto them and blares an alarm until they leave the trigger.

***Patrolling:***

<img width="745" height="558" alt="image" src="https://github.com/user-attachments/assets/c5f80702-657e-45e6-b61f-4a550ea4f83b" />

***Tracking:***

<img width="749" height="568" alt="image" src="https://github.com/user-attachments/assets/d931a90b-1ec2-43e3-9be7-a808cdf146c5" />



> ✅ Use this component to create stealth gameplay, spotlight towers, security patrols, or cinematic lighting effects.

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

In darker environments, standard text and signs can easily fade into the background or become hard to read. Neon lights solve this by adding a vibrant, glowing presence that draws the player's eye. Whether you're labeling locations, guiding players, or adding style to your world, neon lights are both functional and visually striking — perfect for dark, atmospheric spaces

In the dark, a sign in the editor would be hard to read. Adding a dynamic light helps but does give it that neon and shiny look

Sign in the Dark:

<img width="494" height="253" alt="image" src="https://github.com/user-attachments/assets/78f7f4db-f805-4835-9101-27f78acd53af" />

Sign in the Dark with Dynamic light (Better, but doesnt look that great):

<img width="436" height="249" alt="Screenshot 2025-09-10 142245" src="https://github.com/user-attachments/assets/3135dbff-f5af-4e18-9f9d-d8e3d90de6b9" />


Sign with neon and shiny effect (much better):

<img width="415" height="223" alt="image" src="https://github.com/user-attachments/assets/b010d411-f3bf-412a-83a0-79654d9eaa48" />

**What it does:**  
Creates eye-catching focal points and improves visibility.

**How to use it:**
- 
- First, spawn an Environment Gizmo and change the texture to ***Midnight Black***.
  
  <img width="915" height="314" alt="image" src="https://github.com/user-attachments/assets/540c205f-7ba8-4463-8b8c-9885cd89182e" />

- Then click on ***Public Assets***, search for ***Letter a*** and drag the asset named ***Circus Neon Letter A*** into the scene.
  
  <img width="843" height="635" alt="image" src="https://github.com/user-attachments/assets/28550cca-196b-402b-a4ac-ed30c7bed7a6" />

- Click on the asset and to acheive the neon effect we will set the ***Tint Strength*** to 0 and then set the ***Brightness*** to 100.

Before: 

<img width="1349" height="364" alt="image" src="https://github.com/user-attachments/assets/fb542960-8966-43a2-9563-7dc5392a03c7" />

After:

<img width="1364" height="448" alt="image" src="https://github.com/user-attachments/assets/88df223f-3939-4c49-8d13-48e22e75c77e" />

Easy right, no we can add different letters together to make a sign in the example we made a Diner sign.

<img width="689" height="276" alt="image" src="https://github.com/user-attachments/assets/60e9154d-3cc2-492a-8cfe-ee804a93e4d9" />

⚡ Flickering Neon

To make your neon signs feel even more alive — or even a little unstable — you can add flickering effects. This not only enhances realism (like an old sign buzzing with electricity), but also adds personality and atmosphere. A subtle flicker can make your world feel gritty, retro, or even a little haunted, depending on the color and timing you choose.


- To add this effect make a script called ***Flickering_Light*** and then copy this code into it:
  ***Flickering_Light:***
  
```typescript

  import { Entity } from 'horizon/core';
import * as hz from 'horizon/core';

class FlickeringLight extends hz.Component<typeof FlickeringLight> {
  static propsDefinition = {
    meshEntity: { type: hz.PropTypes.Entity }
  };

  private mesh!: hz.MeshEntity;
  private baseBrightness!: number;
  private minBrightness!: number;
  private maxBrightness!: number;

  start() {
    this.mesh = this.props.meshEntity!.as(hz.MeshEntity)!;
    this.baseBrightness = this.mesh.style.brightness.get();
    this.minBrightness = this.baseBrightness * 0.1; // Minimum brightness is 80% of the base
    this.maxBrightness = this.baseBrightness * 1.3; // Maximum brightness is 120% of the base

    this.connectLocalBroadcastEvent(hz.World.onUpdate, this.update.bind(this));
  }

  update(data: { deltaTime: number }) {
    // Randomly vary the brightness between min and max
    const newBrightness = this.minBrightness + (Math.random() * (this.maxBrightness - this.minBrightness));
    this.mesh.style.brightness.set(newBrightness);
  }
}

hz.Component.register(FlickeringLight);
```
- Attach this script to a letter and then edit the min and max brightness to change the range of brightness it flickers between.

  <img width="295" height="99" alt="image" src="https://github.com/user-attachments/assets/ec2d9f0e-fa61-4c5b-8120-e632d072f3eb" />

- Now preview the world and you can see the effect.

  <img width="642" height="342" alt="image" src="https://github.com/user-attachments/assets/d0010c79-3d15-4a11-8dd0-2f1c39310240" />
  (The effect is more prominent in the video).

 ***Bonus:*** This effect can also be used on a dynamic light by changing the intensity instead of the brightness.
- To do this make a new script, copy the code below into the script and then attach it to a dynamic light.

```typescript
 import { Entity } from 'horizon/core';
import * as hz from 'horizon/core';

class FlickeringDynamicLight extends hz.Component<typeof FlickeringDynamicLight> {
  static propsDefinition = {
    
  };

  private light!: hz.DynamicLightGizmo;
  private baseIntensity!: number;
  private minIntensity!: number;
  private maxIntensity!: number;

  start() {
    this.light = this.entity.as(hz.DynamicLightGizmo)!;
    this.baseIntensity = this.light.intensity.get();
    this.minIntensity = this.baseIntensity * 0.8; // Minimum intensity is 80% of the base
    this.maxIntensity = this.baseIntensity * 1.2; // Maximum intensity is 120% of the base

    this.connectLocalBroadcastEvent(hz.World.onUpdate, this.update.bind(this));
  }

  update(data: { deltaTime: number }) {
    // Randomly vary the intensity between min and max
    const newIntensity = this.minIntensity + (Math.random() * (this.maxIntensity - this.minIntensity));
    this.light.intensity.set(newIntensity);
  }
}

hz.Component.register(FlickeringDynamicLight);
```
- This adds the flickering effect to the dynamic light. Which can be used to simulate fire for candle, torches and campfires.


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
