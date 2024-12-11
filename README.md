# CS.11-Summative-Prep-1
Here's a similar problem that tests the same concepts:

```java
/* LibraryBooking System
This class manages study room bookings in a library. The library has 5 study rooms (numbered 1-5),
and each room can be booked for time slots between 9:00 (time slot 0) and 16:00 (time slot 7).
Each time slot is 1 hour long.

A booking request must specify:
- The duration (in hours)
- The desired room or range of rooms
- The start time must be within valid hours
- A booking must be completed within the same room

Complete the following class: */

public class LibraryBooking {
    /* Returns true if the timeSlot in room is available
       Precondition: 1 <= room <= 5; 0 <= timeSlot <= 7 */
    private boolean isTimeSlotFree(int room, int timeSlot) {
        /* implementation not shown */
        return false;
    }

    /* Marks the block of timeSlots starting at startTime for duration hours as reserved
       Precondition: 1 <= room <= 5; 0 <= startTime <= 7; 1 <= duration <= 8 */
    private void reserveBlock(int room, int startTime, int duration) {
        /* implementation not shown */
    }

    /* Part A:
       Find the first available block of consecutive hours in the specified room
       Returns the starting hour if found, -1 if no such block exists
       Precondition: 1 <= room <= 5; 1 <= duration <= 8 */
    public int findFreeTimeBlock(int room, int duration) {
        // To be implemented
        return -1;
    }

    /* Part B:
       Search rooms from startRoom to endRoom for first available block of duration hours
       If found, reserve the block and return true; otherwise return false
       Precondition: 1 <= startRoom <= endRoom <= 5; 1 <= duration <= 8 */
    public boolean makeBooking(int startRoom, int endRoom, int duration) {
        // To be implemented
        return false;
    }
}
```

Example scenario for testing:
```java
Room 1 availability:
9:00-10:00 (slot 0): Available
10:00-11:00 (slot 1): Not Available
11:00-13:00 (slots 2-3): Available
13:00-15:00 (slots 4-5): Not Available
15:00-17:00 (slots 6-7): Available

Room 2 availability:
9:00-12:00 (slots 0-2): Not Available
12:00-14:00 (slots 3-4): Available
14:00-17:00 (slots 5-7): Not Available

Test cases:
1. findFreeTimeBlock(1, 2) should return 2 (11:00)
2. findFreeTimeBlock(1, 3) should return 6 (15:00)
3. findFreeTimeBlock(2, 3) should return -1

makeBooking test sequence:
1. makeBooking(1, 2, 2) should return true and reserve Room 1, 11:00-13:00
2. makeBooking(1, 2, 2) should return true and reserve Room 2, 12:00-14:00
3. makeBooking(1, 2, 3) should return false
```

This problem tests similar concepts:
1. Finding consecutive available time slots
2. Managing reservations across multiple rooms
3. Handling edge cases and constraints
4. Using helper methods effectively
5. Working with time-based scheduling
