# Fashion Wishlist A/B Test Prototype

A clickable high-fidelity prototype for testing three intervention strategies to increase purchase intent on saved wishlists. Built for a Product Management graduation project.

**[🔗 Live Demo](https://raw.githack.com/pavimsc/myntrawishlist/claude/fashion-wishlist-ab-prototype-ua2o3a/index.html)**

---

## The Problem

Users browse fashion products and save them to wishlists, but many wishlisted items never become purchases. The question: **How can we reduce the gap between "I like this" and "I bought this"?**

---

## Three Test Variants

### **CONTROL** (Baseline)
Standard wishlist experience with no intervention.
- Clean product cards
- Simple wishlist with price and save date
- User is on their own to remember and decide

**Insight:** What's the natural conversion rate without help?

---

### **VARIANT A** — Wishlist Engagement Loop
Smart reminders that create urgency and reasons to revisit.

**Timeline (30 days):**
- **Day 1:** "Still thinking about this?" 💭
- **Day 7:** "🔥 Price dropped! Your item is now ₹4XXX"
- **Day 14:** "👀 Popular pick - 23 people bought this recently"
- **Day 21:** "⚠️ Low stock - Only 2 left!"
- **Day 30:** "⏰ Last day of your 30-day reminders"

Each reminder has a 1-click CTA: "View Item"

**Insight:** Does frequent, relevant communication drive purchases?

---

### **VARIANT B** — Wishlist Price Lock
Remove decision anxiety by guaranteeing the customer's price for 30 days.

**On Wishlist:**
- "Your price is locked for 30 days"
- Original locked price (what you saved at)
- Current market price
- Your savings (if price dropped)
- Days remaining on protection

**Insight:** Does price protection reduce friction and increase confidence to buy?

---

## How to Demo (90 seconds)

1. **Open the live link** above
2. **Start with CONTROL:**
   - Click "Control" button (bottom-right)
   - Add 2-3 items to wishlist
   - Navigate to Wishlist tab
   - Notice: Plain, minimal experience
   - Slide day to 30 → nothing special happens

3. **Switch to VARIANT A:**
   - Click "A" button (clears wishlist for fresh test)
   - Add 2-3 items
   - Slide day to 1 → reminder badge appears (pink)
   - Slide to day 7 → different reminder
   - Slide to day 14, 21, 30 → different reminders each time
   - **Key insight:** "It keeps bringing you back"

4. **Switch to VARIANT B:**
   - Click "B" button (clears wishlist)
   - Add 2-3 items
   - Go to Wishlist → see green "Price Locked" box
   - Shows locked price vs market price
   - Slide day to 30 → protection expires
   - **Key insight:** "You feel protected, so you can buy confidently"

---

## Technical Details

**Stack:**
- Single HTML file (no build tools needed)
- Vanilla JavaScript
- CSS Grid + Flexbox (Tailwind-inspired utilities)
- LocalStorage for session state (no backend)

**Features:**
- Three distinct variant UX patterns
- Day slider (0-30) simulates 30-day timeline
- Price simulation (gradual drift)
- Wishlist persistence during session
- Reminder scheduling (Variant A)
- Price lock calculation (Variant B)
- Responsive design (1024px+ desktop focus)

**Browser compatibility:** All modern browsers (Chrome, Safari, Firefox, Edge)

---

## Files

- `index.html` — Complete prototype (single file, ~1000 lines)
- `README.md` — This file

---

## For Your PM Course

**Business Question:**
Which strategy increases wishlist-to-purchase conversion?

**Key Metrics to Track:**
- **CONTROL:** Baseline conversion rate
- **VARIANT A:** Engagement loop effectiveness (reminder click-through, revisit frequency)
- **VARIANT B:** Friction reduction (conversion rate uplift, time to purchase)

**Expected Outcome:**
- Variant A: Higher engagement, more revisits, but may feel pushy
- Variant B: Lower friction, more confident buyers, protection appeals to deal-seekers
- Control: Baseline for comparison

---

## How It Works

### Variant A: Reminders
- Reminders fire on fixed days: 1, 7, 14, 21, 30
- Each reminder is contextual (price drops, low stock, social proof, last call)
- Shown as prominent pink badge on wishlist item
- User can click "View Item" CTA to revisit product

### Variant B: Price Lock
- Original price locked when item is wishlisted
- Current market price simulates gradual decline (2% per day)
- System calculates savings: locked price - market price
- Protection countdown: "Expires in X days"
- Expires at Day 30

### Day Slider
- Simulate time progression without waiting
- All prices, reminders, and countdowns update in real-time
- Switch between variants with wishlist reset (clean test)

---

## Experiment Controls

Bottom-right corner of the app:

- **Variant:** Choose Control / A / B
- **Day slider:** 0-30 (simulates timeline)
- **Reset button:** Clear wishlist, reset day to 0
- **Status display:** Current variant, day, wishlist count

---

## Next Steps for Your Project

1. **Present the prototype** to show the three concepts visually
2. **Discuss trade-offs:**
   - Variant A pros: Engagement, top-of-mind
   - Variant A cons: Can feel spammy, pushy
   - Variant B pros: Removes anxiety, decision-making friction
   - Variant B cons: Risky if prices go up
   - Control: Baseline, user-driven

3. **Propose measurement plan:**
   - Random assign users to variant
   - Track: wishlist adds, revisits, purchases, time-to-purchase
   - Run for 30 days
   - Measure: conversion rate uplift, customer satisfaction

4. **Recommend winner** based on primary metric (e.g., conversion rate)

---

## Questions?

This prototype demonstrates the core mechanic of each strategy. Feel free to:
- Adjust prices, stock levels, or reminder messages
- Test different day combinations
- Share with classmates to get feedback

---

**Built for:** PM Graduation Project  
**Status:** Prototype / Demo Ready  
**Last Updated:** 2026-08-21
