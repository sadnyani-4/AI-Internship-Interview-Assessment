# Assessment 2: Scenario-Based Assessment

## Problem Statement
Schedula needs to implement an Intelligent Queue Management system for a medical practice with the following characteristics:
- 50 doctors with varied scheduling patterns
- Each doctor sees 30-50 patients daily in 3-hour blocks
- Patients arrive unpredictably, often not at their scheduled times
- Appointments come from multiple channels (IVR, app, WhatsApp)
- Walk-in patients need to be accommodated
- Some doctors track patient status (arrived, waiting, consulted), but not all

## 1. Problem Breakdown

### Logical Components & Steps

#### **Doctor Management**
- **Manage Individual Doctor Availability**: I created a `Doctor` class to hold each doctor's information, including their availability and patient queue. 
- **Real-Time Updates**: The `QueueManagementSystem` class dynamically updates patient queues as patients check in and their statuses are updated.

#### **Patient Arrival & Appointment Handling**
- **Scheduled vs. Actual Arrival Times**: The system logs both scheduled appointment times and actual patient arrivals through the `Patient` class, allowing for the calculation of priority based on urgency and delays.
- **Handling Walk-In Patients**: A method for assigning patients, including walk-ins, is integrated into the queue management system to ensure minimal disruption.

#### **Multi-Channel Appointment Sources**
- **Appointment Integration**: The system supports various appointment sources by allowing patients to be assigned from multiple channels (IVR, app, WhatsApp, and walk-ins).

#### **Queue Optimization & Prioritization**
- **Dynamic Queue Assignment**: Patients are assigned to doctors based on urgency, real-time queue lengths, and availability. Patient priority is calculated by the `Patient` class considering both urgency and delay from scheduled times.
- **Utilize Historical Data**: Although the current implementation does not store historical data, analyzing patient flow in future versions could enhance decision-making during peak times.

#### **Patient Status Tracking**
- **Real-Time Status Updates**: The system provides real-time updates for patients marked as “arrived,” “waiting,” or “consulted” through the status management in the `Patient` class.

## 2. Required Information for Intelligent Queuing
- **Doctor's Live Schedule & Consultation Durations**: The system utilizes real-time data regarding doctor availability and estimated consultation times to assist in queue management.
- **Real-Time Patient Check-In & Arrival Patterns**: The `QueueManagementSystem` tracks everything in memory, logging check-ins and arrival times as patients are processed.
- **Historical Appointment Data**: While this implementation does not include historical appointment data, future enhancements could integrate recorded data to identify peak times.
- **Channel-Wise Booking Trends**: The system currently integrates multiple channels for booking but does not yet analyze trends.
- **Doctor-Specific Queue Preferences**: The current version showcases how patient assignments can be managed through urgency levels, which could be enhanced in future versions.

## 3. Measuring System Effectiveness
- **Average Wait Time Reduction**: Future implementations should measure wait times before and after the system's implementation to assess improvement.
- **Queue Efficiency Score**: Metrics such as patients served per doctor during each time block can help validate system efficiency.
- **Patient Satisfaction Metrics**: Implementing feedback mechanisms, such as surveys or forms, could gather insights about patient experience.
- **No-Show & Walk-In Handling**: The current implementation tracks patient arrivals and status changes, allowing for analysis of systems effectiveness in managing unexpected patients.

## 4. Patient Communication Strategy
- **Real-Time ETA Updates**: The system can be enhanced to provide patients with estimated wait times through notifications.
- **Rescheduling Option**: Automatic rescheduling options can be introduced for patients experiencing lengthy wait times.
- **Check-in Confirmation**: The current system includes a confirmation feature for patients when the doctor is ready for them.

## Loom Video Demonstration
You can view the video demonstration of my assessment [here](https://www.loom.com/share/d48e8cde826a4d3c871a5f8c7d9d1c54?sid=841ffe67-3d5f-45f9-b4a7-bffae656184c).