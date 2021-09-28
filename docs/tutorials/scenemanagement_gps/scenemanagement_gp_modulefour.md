---
id: scenemanagement-gp-four
title: Netcode Scene Management Golden Path - Module Four: Additive Scene Loading
sidebar_label: Golden Path Module Four
---
In this guide, we cover:
* Loading scenes additively
* Receiving SceneEvent notifications
* The foundation for additional scene management Golden Paths

## Prerequisites

You should have completed the foundation module [here](goldenpath_foundation_module.md) before starting this tutorial.

### Create a Clone of the foundation 'GoldenPath' project

import Createclone from '../../shared/_create_clone_goldenpath.md';

<Createclone/>

## Open GoldenPath_Four

1. Open your **Unity Hub**.
2. Select `GoldenPath_Four` from your projects.

## Creating Scenes

1. Create a new scene by going to **File** > **New Scene**.
2. Select the **Basic (Built-in)** template and name it `MainScene_Example1`. This creates a scene without directional light and camera. To name your scene, you need to **Save** or **Save as** your scene from either the **File** dropdown or the vertical ellipsis of the scene in the **Hierarchy** tab.
   :::tip
   Make sure your scene is being saved in the **Assets** > **Scenes** folder.
   :::
3. Create a second scene, but this time select the **Empty (Built-in)** template and name it `SceneToLoad_Example1`. This creates a scene without directional light and camera.
   :::tip
   You can open the `SceneToLoad_Example1` with `MainScene_Example1` open by dragging `SceneToLoad_Example1` into the **Hierarchy** tab with `MainScene_Example1`. This is called [multi-scene editing](https://docs.unity3d.com/Manual/MultiSceneEditing.html).
   :::
4. Add a sphere to the root of the `SceneToLoad_Example1` scene by right-clicking in the **Hierarchy** tab, hovering over **3D Object**, and selecting **Sphere**. Ensure the sphere is positioned as X=0, Y=0, and Z=0 so it is visible when loaded.

<!-- Add video here after UI updates -->

## Create a NetworkManager GameObject

1. From the **Hierarchy** tab, right-click `MainScene_Example1`, hover over **GameObject**, select **Create Empty**, and name it **NetworkManager**.
2. With the **NetworkManager** GameObject selected, click on **Add Component** from the **Inspector** tab, select **MLAPI** > **NetworkManager**.
3. Select **UNet** for your **NetworkTransport**.
4. Scroll near the bottom of the **NetworkManager** component and ensure **Enable Scene Management** is checked.

<!-- Add video here after UI updates -->

## Add UI GameObjects

We are going to add UI canvas and button GameObjects to our `MainScene_Example1`.

1. From the **Hierarchy** tab, right-click `MainScene_Example1`, hover over **GameObject** > **UI**, select **Canvas**, and leave it named **Canvas**. An **EventSystem** is created with the **Canvas** object.
2. Right-click on your newly created **Canvas**, hover over **GameObject** > **UI**, select **Button**, and name it **LoadScene**. A **Text** object is created under the **Button** object.
3. Select the **Text** of your newly created **Button**. In the **Inspector** tab, in the **Text** box, change `Text` to `Load Scene`.
4. Select the **LoadScene** object and set the position of the button from the **Inspector** tab under **Rect Transform**. 
   1. Click on the **Anchor Presets** grid icon. Set the anchor so it is `top` and `center`.
   2. Set the coordinates to Pos X=0, Pos Y=-20, and Pos Z=0.

<!-- Add video here after UI updates -->

## Add the SceneLoader Script

1.

## Test Verification One

## Test Verification Two

:::contribution Special Thanks
This guide would not have been possible without the hard work and support of Noel Stephens, Unity.
:::