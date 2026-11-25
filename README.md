# ShadowNet: An AI-Assisted Offline Emergency Communication Network Using BLE

## 1. Project Purpose

ShadowNet is an Android-based offline emergency communication application designed to help people communicate during natural disasters, network failures, and emergencies in remote areas.

The application uses Bluetooth Low Energy (BLE) to exchange messages between nearby smartphones without requiring mobile data or an internet connection.

Its main purpose is to provide an additional communication option when normal network services are unavailable.

### Main Features

- **Offline Messaging:** Send and receive messages without internet access.
- **Emergency SOS:** Send emergency alerts with an optional location.
- **Multi-Hop Message Forwarding:** Forward messages through intermediate smartphones.
- **Delivery Acknowledgement:** Track message delivery and confirmation.
- **Emergency Priority Classification:** Classify messages into medical, fire, flood, and general help categories.
- **Local Message Storage:** Save messages on the device for future access and forwarding.

## 2. Architecture

ShadowNet follows a decentralized communication approach in which participating smartphones exchange messages using Bluetooth Low Energy.

<img width="1118" height="1600" alt="WhatsApp Image 2026-11-25 at 12 12 59 PM" src="https://github.com/user-attachments/assets/c6c8018a-8213-4af5-aa0d-4d25c15a814b" />




### Working Process

1. The user creates a normal message or emergency SOS alert.
2. The application assigns a message ID and stores it locally.
3. BLE discovers nearby ShadowNet devices.
4. The message is transferred to a nearby device.
5. The receiving device checks for duplicate messages and saves the new message.
6. If required, the receiving device forwards the message to another nearby device.
7. Delivery acknowledgement is used to update the message status.

### Technologies Used

| Technology | Purpose |
|---|---|
| Kotlin | Android application development |
| Android Studio | Development environment |
| Bluetooth Low Energy | Offline device communication |
| Room / SQLite | Local message storage |
| Android Location API | Emergency location sharing |
| TensorFlow Lite / LiteRT | Optional AI-based classification |

## 3. Setup

### Requirements

- Android Studio
- Kotlin development support
- Android smartphone with BLE support
- Android SDK
- Two or more Android smartphones for testing
- Bluetooth permission enabled

### Installation Steps

1. Install Android Studio on your computer.
2. Clone or download the ShadowNet project repository.
3. Open the project in Android Studio.
4. Allow Gradle to sync and download required dependencies.
5. Connect an Android smartphone using USB debugging.
6. Build and run the application.
7. Install the application on another Android smartphone for communication testing.
8. Grant the required Bluetooth and location permissions.

### Run the Application

```bash
git clone <https://github.com/Monishkumar20/mini-project>
```

Open the downloaded project in Android Studio and click **Run**.

## 4. Usage

1. Open the ShadowNet application on two or more Android smartphones.
2. Enable Bluetooth on all participating devices.
3. Grant the required application permissions.
4. Start nearby device discovery.
5. Select a nearby ShadowNet device or use the emergency SOS option.
6. Enter a message or select an emergency category.
7. Send the message using BLE.
8. The receiving device stores and displays the message.
9. Intermediate devices can forward messages when multi-hop forwarding is implemented.
10. Check the delivery status and acknowledgement.

### Example Scenario

Phone A sends an emergency SOS message.

Phone B receives and forwards the message.

Phone C receives the forwarded emergency alert.

```text
Phone A  --->  Phone B  --->  Phone C
  SOS          Relay        Receive
```

This demonstrates the proposed offline message-forwarding workflow.

## 5. Results

The expected output of ShadowNet is an Android application that can demonstrate:

- Offline message exchange between nearby smartphones.
- Emergency SOS message transmission.
- Local storage of messages and alerts.
- Message forwarding through intermediate devices.
- Emergency priority classification.
- Delivery acknowledgement and status tracking.

### Performance Evaluation

The application will be evaluated using:

| Evaluation Parameter | Purpose |
|---|---|
| Message Delivery Success Rate | Measure successful message delivery |
| Message Delivery Time | Measure the time taken to deliver messages |
| Relay Hops | Count the intermediate devices used |
| Battery Consumption | Observe battery usage during communication |
| Message Reliability | Check duplicate handling and delivery confirmation |

*Note: These are evaluation objectives. Actual results and measurements should be added after implementing and testing the application.*

## 6. Reflection

Through the development of ShadowNet, we aim to learn Android application development, Bluetooth Low Energy communication, local database management, and offline networking concepts.

Working as a two-member team will help us improve our teamwork, problem-solving, and software integration skills.

### Challenges We Aim to Solve

- Establishing BLE communication between multiple smartphones.
- Handling Bluetooth permissions and device compatibility.
- Forwarding messages without creating duplicates.
- Storing emergency messages when devices are disconnected.
- Managing message delivery acknowledgements.
- Prioritizing emergency messages.

### What We Learned

This project will help us understand how mobile devices can communicate without internet connectivity and how decentralized message forwarding can support emergency communication.

It will also provide practical experience in developing Android applications and testing communication protocols.

---

## Future Enhancements

- Improved AI-based emergency classification.
- Battery-aware message forwarding.
- Offline maps and safe-zone information.
- Emergency volunteer and resource coordination.
- Improved message encryption and privacy.

## Conclusion

ShadowNet proposes an offline emergency communication solution using Bluetooth Low Energy. By combining offline messaging, SOS alerts, local storage, message forwarding, and emergency priority classification, it aims to provide an alternative communication method during network outages and emergency situations.
:::
