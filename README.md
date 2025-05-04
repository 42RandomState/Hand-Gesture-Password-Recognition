# Hand Gesture Password Recognition 

This project allows users to unlock access using a **4-digit hand gesture password**, recognized via a webcam and the MediaPipe library. It uses the **left hand** to input the password and the **right hand** to delete or reset inputs. Face detection is also used for added security.

--

## How It Works

- When you run the script, you will be prompted to enter a **4-digit password** using digits from `0` to `4`.
- Each digit corresponds to the number of fingers shown on your **left hand**:
  - `0`: Fist (no fingers)
  - `1`: One finger
  - `2`: Two fingers
  - `3`: Three fingers
  - `4`: All fingers open (excluding thumb)
- Show one gesture at a time. If stable for ~1 second, it will be recorded.
- Use your **right hand** to:
  - Delete the last digit (if entered)
  - Reset the password entry (if all 4 digits are wrong)

- You have **3 total attempts**. If the password is incorrect after 3 tries, access is denied and a screenshot of the "intruder" is saved.
- If the password is correct, access is granted and a screenshot is saved as proof.
