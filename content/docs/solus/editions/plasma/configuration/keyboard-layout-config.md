---
title: "Keyboard Layout Configuration"
date: 2023-09-10
draft: false
weight: 211
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

## Using System Settings

{{< alert context="warning" text="If you need to input languages that do not use Latin characters (for example, Chinese or Japanese), use IBus instead." />}}

1. In the [System Settings](../open-system-settings) screen, go to **Input Devices** > **Keyboard** > **Layouts**.

   The layouts screen appears.

   ![Keyboard layouts screen.](../img/keyboard-layouts.png)

2. Select **Configure layouts**.
3. Configure keyboard layouts as you need.

   - To add a keyboard layout click **Add**, select a layout from the list, and click **OK**.
   - To remove a keyboard layout select a layout from the list and click **Remove**.
   - To order the list of keyboard layouts, select a layout from the list, then use the **Move Up** and **Move Down** buttons to reorder the list.

4. Configure a keyboard shortcut to switch between layouts by using the options under **Shortcuts for Switching Layout**.

   - To use the default shortcuts Solus Plasma provides, use the **Main shortcuts** and **3rd level shortcuts** options.
   - To use a custom shortcut, use the **Alternative shortcut** option.

5. Click **Apply**

## Using IBus

Solus Plasma includes IBus installed by default. However, you need to enable and integrate IBus with Plasma before usage.

{{< alert context="warning" text="Using IBus overrides the configuration in the **Layouts** section of **System Settings**" />}}

1. Open the `/home/[username]/.bashrc` file with a text editor.
2. Add the following lines at the end of the file.

   ```bash
   export GTK_IM_MODULE=ibus
   export QT_IM_MODULE=ibus
   export XMODIFIERS=@im=ibus
   ```

3. Save the file.
4. Configure IBus to autostart.
   - In the [System Settings](../open-system-settings) screen, go to **Workspace** > **Startup and Shutdown** > **Autostart**.
   - Click **Add**, then **Add Application**.
   - In the search box, enter `ibus-daemon -rxR` and click **OK**.
5. Log out from your session, then log in again.
6. Configure keyboard layouts as you need.
   - Open IBus Preferences from the application launcher.
   - In the Input Method tab, add the keyboard layout you need.

{{< alert context="warning" text="Some keyboard layouts require installing additional packages." />}}