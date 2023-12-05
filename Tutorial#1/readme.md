# Tutorial#1: Image Hide-and-Seek

Welcome to our app development tutorial! This guide is tailored for beginners who are just embarking on their exploration of the app development world using a low/no-code approach. Throughout this tutorial, we will be utilising the [MIT App Inventor](https://appinventor.mit.edu/) platform to craft and shape our app.

> [!IMPORTANT]
> If you are solely interested in building and testing the app, feel free to skip ahead to the [Building Your First App section](#building-your-first-app). You can download the project [HERE](./download/tutorial-1.aia) and open it in the MIT App Inventor platform.

## Prerequisites
To get started, make sure you have the following:
1. A computer (laptop or desktop) with internet connection.
2. A Gmail address for logging into the MIT App Inventor website.
3. An Android phone or tablet for testing the app.
4. Install the [MIT AI2 Companion app](https://play.google.com/store/apps/details?id=edu.mit.appinventor.aicompanion3) on your Android device.
5. Optionally, you can use a USB cable and [aiStarter](https://appinventor.mit.edu/explore/ai2/setup-emulator.html).

## Learning Objectives
By the end of this tutorial, you will gain proficiency in:
1. Navigating the MIT App Inventor platform.
2. Designing basic user interfaces.
3. Constructing logical processes based on your designs.
4. Testing and sharing the app through at least two different methods.

# Setup
The setup process is a one-time task, and depending on the availability of hardware and internet connectivity, the steps may vary slightly. However, here are the common steps you need to follow to set up your environment.

1. **Gmail Address:** You will need a Gmail address to log in to your account. Every computer should use unique Gmail address.
> [!CAUTION]
> It is not recommanded to use the same Gmail address to log in into multiple computers. Potentially, you will destroy other people's work.

2. **Install MIT AI2 Companion App:** Head over to the Play Store and install the MIT AI2 Companion app. This app enables you to test your app on an actual Android device.

3. **Install aiStarter:** If you plan to connect a phone/tablet to your computer using a USB cable, install aiStarter on your computer.

These steps, once completed, will ensure that your environment is set up for a smooth app development experience. Remember to adapt the process according to your hardware and internet availability.

# Building your First Mobile App

## User interface design

Let's begin by designing the user interface. Below is a hand-drawn diagram illustrating how the interface should look:

![user interface](media/layout.jpg)

Now, we will guide you through the process of building this interface using the MIT App Inventor platform. Follow these steps:

1. Visit [MIT APP Inventor](https://appinventor.mit.edu/) using a web browser and click on the `Create Apps!` button.
2. Log in using your Gmail address.
3. For the first-time login, it might show you an introduction; you can skip it by ticking off a box.
4. Click on the `Start new project` button, name your project (choose a name aligned with your app's functionality).
5. After a moment, your project will be ready, and you will see the interface with four panels. Let's understand them:
    > ![MIT1](media/MIT%20App%20Inventor_1.png)

    > - **Panel 1:** User interface and layout, separated into different sections.
    > - **Panel 2:** Drag-and-drop area for various components, with the option to change screen sizes.
    > - **Panel 3:** Tree view of draggable components. Below it is the `Media` panel for uploading assets.
    > - **Panel 4:** Modify properties of selected components.

6. Drag and drop an `Image` and a `Button` onto your screen, resulting in the following layout:
   ![MIT2](media/MIT%20App%20Inventor_2.png)
7.  Adjust the components' positions to the center and middle of the screen:
    > - Click on `Screen1` in the `Components` tree.
    
    > - Set `AlignHorizontal` and `AlignVertical` to `Center` in the `Properties` panel.

    > *Optional*: To use the device default theme, scroll down in the `Properties` panel and change the `Theme` to `Device Default`.
8.  The `Image` component is a placeholder; upload an actual image:
    > - Go to the `Media` panel, click `Upload File`, and select `light_on.png` from the `media` folder.

    > - Click on the image icon or `Image1` in the `Components` tree. In the `Properties` panel, click `Picture`, select your image file, and press `OK`.

    >  - To prevent the image from dominating the screen, set its height to a percentage value (e.g., 60%) in the `Properties` panel.
9.  Customise the `Button`:
    > - Click on the `Button` on the screen.
    > - In the `Properties` panel, set the `Width` to `Fill parent`.
    > - Change the `Text` property to *Hide*.
10. **Congratulation!** You have completed the design phase. Now, it's time to think about implementing the app logic.

## App logic
The app logic is responsible for toggling the visibility of the image and updating the button text accordingly. Follow these steps to implement the logic:

![logic](media/logic.jpg)

1. Navigate to the `Blocks` tab above the `Properties` panel.
2. Click on `Button1` in the `Blocks` panel and drag the `when Button1.Click` block.
3. Drag an `if then else` block from the `Control` section into the `when Button1.Click` block.
4. Drag an equal block from the `Logic` section and drop it into the if statement.
5. Use the `Button1.Text` block from the `Button1` section, placing it in the first section of the equal operation.
6. Drag an empty text block from the `Text` section into the second part of the equal operation. Type *Hide* in the empty block.
   ![block-code-1](media/blocks1.png)
7. Click on the `Image1` block and drag and drop `set Image1.Visible to` on your screen. From the `Logic` section grab the `False` block. Connect them together.
8. Similarly, click on the `Button1` block and drag and drop `set Button1.Text to` on your screen. From the `Text` section grab the empty text block and type `Show`. Connect them together.
9. Move these two blocks inside the if statement.
   ![block-code-2](media/blocks2.png)
9. Right-click on the first set block, choose `Duplicate`, and move the duplicated block inside the else statement. Change `False` to `True` and `Show` to `Hide`.
10. Duplicate the other block, move it into the else statement, and change the text to *Hide*. The final code is as follows:
    ![final code](media/blocks3.png)
11. **Congratulations, you are done!** Test your app to see the logic in action.

## Testing the app
Testing your app is a crucial step in ensuring its functionality. Here is the simplest way to test your app. Ensure that your laptop and tablet/mobile devices are connected to the same Wi-Fi network.

Follow these steps to test the app:
1. Click on `Connect` and select `AI Companion`. This action generates a QR code.

    ![MIT3](media/MIT%20App%20Inventor_3.png)

2. Open the `MIT AI2 Companion` app on your phone/tablet and choose `Scan QR code`.
3. Point your camera at the QR code and hold it until the scanning process is complete.
4. Your app should load on your mobile device, and it should now be operational.

This method provides a quick and efficient way to test your app on a physical device, allowing you to experience its functionality as intended.

## Extension activity 1
You may notice that the show/hide button jumps up and down on the screen when you click on it. Though, it is not a big problem but it does not feel good. Remember what I mentioned earlier about user experiences? You need to provide a smooth experience to your user. Certainly, this app fails to deliver it. So it is the time to fix it. Let's do it!

**Caution: You may lose your code if you proceed. To save your code, go to the `Blocks` tab, right-click on your code and select `Add to Backpack`. This will save the code in the backpack and you can retrive it latter.**

### **Fixing the jumping button**
1. Return to the `Designer` tab and delete the `Image` and the `Button` from the screen. You will have en empty screen again.
   > You may get an warning message similar to the following image. Click on `Save the empty screen now.` button.
   ![MIT4](media/MIT%20App%20Inventor_4.png)
2. Click on the `Layout` tab from the left panel and drag and drop two `VerticalArrangement` block on the screen.
   > Layout helps to create a container where you can arrange multiple components. You can arrange multiple buttons in an `HorizontalArrangement` to create a navigation panel and so on.
3. Click on the top container and from the `Properties` panel change the `Height` to 80% and `Width` to *fill parent*.
4. Click on the other container and from the `Properties` panel change the `Width` to *fill parent*.
5. Drag and drop an `Image` component into the top container. Click on the `VerticalArrangement1` from the components panel and align it to center for both horizontal and vertical.
6. Drag and drop a `Button` component into the other container. Click on the `VerticalArrangement2` from the components panel and align it to center for both horizontal and vertical.
7. Click on the `Image` component and choose the uploaded image.
   > You can optionally change the `Height` property of the image if you would like to do so.
8. Change the button `Width` to *fill parent* and change the `Text` to *Hide*.
9. Go to the `Blocks` screen and click on the backpack icon. Drag and drop the code into the code area.
10. **You are done!**. Test it out.

---
## Extension activity 2
The next posible activity could be adding a sound assest. Follow these steps to add a sound file with the button component.

1. From the left panel, Click on the `Media` tab and drag and drop `Sound` component on the screen. Sound is a *non visible* component, so you cannot see anything on the screen.
2. Upload a **WAV** sound file, the same as you have uploaded the image file.
    > You will find a sound file (`switch-1.wav`) inside the `media` folder.
3. Click on the `Sound1` from the `Components` tree and from the `Properties` panel, select the uploaded sound file as a `Source`.
4. Move to the `Blocks` tab and click on the `Sound1` and drag `call Sound1.Play`.
5. Move the `Play` block inside the `if` and `else` part. The final code looks like the below.
![block 5](media/blocks4.png)


<p align='center'> All done!!! </p>
