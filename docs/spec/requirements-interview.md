# SnapSpot Requirements Interview

**Purpose:** Clarify requirements and assumptions before writing formal product specification.

**Instructions:** Answer the questions below. Focus on the ones you have strong opinions about - we can mark others as "unknowns" for future exploration.

---

## **PART 1: Problem & Vision**

### 1. Why does SnapSpot need to exist?
What specific pain point triggered this idea? Have you personally experienced this problem as a tourist or seen others struggle with it?

**Your Answer:**
<!-- Write your answer here -->

---

### 2. Market validation
Have you talked to any tourists or photographers about this concept? What was their reaction to the "work for free" model?

**Your Answer:**
<!-- Write your answer here -->

---

### 3. Competitive landscape
Are you aware of similar services like Flytographer, Shoott, or local photography services? How is SnapSpot fundamentally different beyond the "free" aspect?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 2: User Segments & Behavior**

### 4. Tourist Profile
- Are we targeting solo travelers, couples, families, or all?
- Age range? Tech-savvy millennials or broader?
- Domestic tourists or international visitors?
- What's their typical photo need: single landmark shot, mini photoshoot, or day-long coverage?

**Your Answer:**
<!-- Write your answer here -->

---

### 5. Photographer Profile
- Amateur enthusiasts, photography students, semi-pros, or all levels?
- Minimum equipment requirements? (Just phone? DSLR required?)
- Age restrictions? Background check requirements?
- Geographic focus: major tourist cities first, or everywhere?

**Your Answer:**
<!-- Write your answer here -->

---

### 6. Critical Assumption
What evidence do you have that photographers will consistently work for free? What happens if they start asking tourists for "tips" outside the app?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 3: Core Mechanics**

### 7. Matching System
- How quickly must a match happen? (Instant like Uber? Schedule ahead?)
- Maximum radius for matching? (Walking distance? 5km? 10km?)
- Can tourists browse photographer profiles or is it purely algorithmic?
- Can photographers decline requests? How many before penalties?

**Your Answer:**
<!-- Write your answer here -->

---

### 8. Session Logistics
- How long is a typical photo session? (5 min quick shot? 30 min session?)
- How many photos minimum must photographer deliver?
- Who owns the photo rights?
- How are photos delivered? (In-app? Email? Instagram DM?)

**Your Answer:**
<!-- Write your answer here -->

---

### 9. Gamification Specifics
- What actions earn points? (Sessions completed? Ratings? Speed of response?)
- What privileges do higher levels unlock?
- Can photographers lose points/levels for bad behavior?
- Are leaderboards global, city-based, or category-based?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 4: Trust & Safety**

### 10. Safety Concerns
- How do we verify photographer identity?
- What if photographer doesn't show up? Or tourist doesn't?
- Rating system: Both sides? What constitutes removal from platform?
- Emergency features? (Share location? Panic button?)

**Your Answer:**
<!-- Write your answer here -->

---

### 11. Quality Control
- How do we ensure photo quality without payment leverage?
- Can tourists request re-shoots if unhappy?
- Portfolio requirements to join as photographer?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 5: Technical & Operational**

### 12. Platform Decision
You mention "mobile web app" - why not native iOS/Android? Is this for faster MVP or strategic choice?

**Your Answer:**
<!-- Write your answer here -->

---

### 13. Real-time Requirements
- Define "real-time" - responses within 1 second? 10 seconds? 1 minute?
- Expected concurrent users at launch?
- Geographic launch: One city? One country? Global?

**Your Answer:**
<!-- Write your answer here -->

---

### 14. Instagram Integration
- How do we verify photographers actually tag/mention tourists?
- Is Instagram API integration required or manual process?
- What if tourist doesn't have Instagram?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 6: MVP Scope**

### 15. Essential vs. Nice-to-Have
From this list, mark each item as **"MVP Essential"** or **"Future"**:

- [ ] User registration/profiles
- [ ] Real-time matching
- [ ] In-app messaging/chat
- [ ] Photo delivery system
- [ ] Rating system
- [ ] Points/levels system
- [ ] Leaderboards
- [ ] Push notifications
- [ ] Schedule-ahead bookings
- [ ] Photographer portfolio galleries
- [ ] Tourist trip histories
- [ ] Social sharing features
- [ ] Multi-language support
- [ ] Payment system for future premium features

**Your Answer:**
<!-- Mark each with [MVP Essential] or [Future] next to the checkbox -->

---

### 16. Success Metrics
What defines a successful MVP launch?
- Number of completed sessions?
- User retention rate?
- Geographic coverage?
- Average session rating?

**Your Answer:**
<!-- Write your answer here -->

---

## **PART 7: Constraints & Risks**

### 17. Timeline
When do you need the MVP live? Any specific deadline (summer tourist season)?

**Your Answer:**
<!-- Write your answer here -->

---

### 18. Resources
What's your team size/composition? Budget constraints?

**Your Answer:**
<!-- Write your answer here -->

---

### 19. Legal Concerns
Have you considered liability for meetups? Terms of service requirements?

**Your Answer:**
<!-- Write your answer here -->

---

### 20. Failure Modes
What's your biggest fear about this concept? What would make you pivot or shut down?

**Your Answer:**
<!-- Write your answer here -->

---

## Next Steps

After you complete this interview:
1. Save this file
2. Commit to git: `git add docs/spec/requirements-interview.md && git commit -m "Complete requirements interview"`
3. Let spec-analyzer know you're done
4. spec-analyzer will produce a **Spec Brief** (1-2 pages)
5. spec-writer will create formal product specification
