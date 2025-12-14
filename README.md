# QuickkShop Configuration Guide

**Welcome!** This guide will help you edit the shop items for our server. Don't worry if you're not tech-savvy - we'll walk through everything step by step.

## Quick Reference (For Returning Users)

**Already done this before? Here's the quick version:**

1. Go to YOUR fork (YourUsername/QuickkShop)
2. Click `shop.yml` → Edit (pencil icon)
3. Make changes → Scroll down
4. Write commit message → Commit changes
5. Click "Contribute" → Open pull request → Create pull request
6. Done! Wait for admin review

**First time? Scroll down for the full guide!**

---

## Table of Contents
- [How to Edit on GitHub (Start Here!)](#how-to-edit-on-github-start-here)
- [Understanding the Shop File](#understanding-the-shop-file)
- [How to Change Prices](#how-to-change-prices)
- [How to Add New Items](#how-to-add-new-items)
- [How to Add Color to Names](#how-to-add-color-to-names)
- [Understanding Slots (Positions)](#understanding-slots-positions)
- [Common Mistakes to Avoid](#common-mistakes-to-avoid)
- [Reference: All Settings Explained](#reference-all-settings-explained)

---

## How to Edit on GitHub (Start Here!)

**First time?** Don't worry! This guide will walk you through EVERYTHING, even if you've never used GitHub before.

### What You Need to Know First

When you suggest changes to the shop file:
1. You'll make a copy of the file (called a "fork")
2. You'll edit your copy
3. You'll ask an admin to review your changes (called a "pull request")
4. If approved, your changes go live!

This keeps the shop safe - nothing breaks unless an admin approves it first.

---

## Complete Step-by-Step Guide

### Part 1: Create a GitHub Account (One-Time Setup)

**Skip this if you already have a GitHub account!**

1. Go to https://github.com
2. Click the "Sign up" button (top right)
3. Enter your email, create a password, and choose a username
4. Verify your email address
5. Done! You now have a GitHub account

---

### Part 2: Fork the Repository (Make Your Copy)

**You only need to do this ONCE. After that, you can skip to Part 3.**

1. Go to the shop repository (the link your admin gave you)
2. **Make sure you're logged in** to GitHub (your username should show in the top right)
3. Look for a button called **"Fork"** in the top-right area of the page
4. Click the **Fork** button
5. GitHub will ask you to confirm - click **"Create fork"**
6. Wait a few seconds while GitHub copies everything
7. Done! You now have your own copy of the shop file

**How to know if it worked:** You should see your username in the top-left, like `YourUsername/QuickkShop` instead of the original repository name.

---

### Part 3: Edit Your Copy of shop.yml

Now you'll make changes to YOUR copy:

1. **Make sure you're in YOUR fork** (should say YourUsername/QuickkShop at the top)
2. Click on the file called **`shop.yml`**
3. Click the **pencil icon** (✏️) on the right side - it says "Edit this file" when you hover over it
4. Make your changes!
   - Change prices
   - Add new items
   - Update colors
   - Whatever you need to do
5. **Double-check your spacing** - this is super important!

---

### Part 4: Save Your Changes (Commit)

After editing:

1. Scroll down to the bottom of the page
2. You'll see a box that says **"Commit changes"**
3. In the first text box, write a short description of what you changed
   - Good examples: "Increased diamond prices", "Added copper ore to shop", "Fixed wheat seed price"
   - Bad examples: "update", "changes", "idk"
4. Leave the second box empty (you can add more details if you want, but it's optional)
5. Make sure **"Commit directly to the main branch"** is selected
6. Click the green **"Commit changes"** button

Your changes are now saved to YOUR copy!

---

### Part 5: Submit a Pull Request (Ask Admin to Review)

Now you need to ask an admin to add your changes to the real shop file:

1. **Go to YOUR fork** (YourUsername/QuickkShop)
2. You should see a yellow banner that says **"This branch is 1 commit ahead"** with a button
3. Click the **"Contribute"** button (or "Pull request" button)
4. Click the green **"Open pull request"** button
5. You'll see a form:
   - **Title:** Write what you changed (e.g., "Updated diamond and gold prices")
   - **Description:** Explain WHY you made the changes (optional but helpful!)
   - Example description: "Diamonds were too cheap, raised the price. Gold was too expensive for new players, lowered it."
6. Click the green **"Create pull request"** button
7. **Done!**

An admin will now review your changes. You'll get a notification when they approve it or if they have questions.

---

### Part 6: Making More Changes Later

After your first pull request, if you want to make MORE changes:

**Option A: If your last pull request is still waiting for review**
1. Go to YOUR fork
2. Edit the `shop.yml` file again (pencil icon)
3. Make your new changes
4. Commit them
5. They'll automatically be added to your existing pull request!

**Option B: If your last pull request was already approved**
1. Go to YOUR fork
2. You might need to sync it first - look for a button that says **"Sync fork"** and click it
3. Then follow Parts 3-5 again (Edit → Commit → Pull Request)

---

## Visual Checklist for Pull Requests

Before clicking "Create pull request", make sure:
- ✅ You described what you changed
- ✅ You checked your spacing/indentation
- ✅ You didn't accidentally delete anything important
- ✅ Your material names are spelled correctly
- ✅ Your prices make sense (no negative numbers unless intentional)

---

## Important GitHub Tips

### Spacing is CRITICAL
- Each line's spacing matters - don't add or remove spaces at the start of lines
- Copy an existing item's spacing if you're unsure

### Don't Panic!
- If you make a mistake, admins can reject your pull request
- Nothing breaks until an admin approves your changes
- You can always close a pull request and start over

### Be Descriptive
- Good commit message: "Increased iron price from 500 to 750"
- Bad commit message: "changes"

### Ask Questions
- Not sure about something? Ask an admin BEFORE submitting
- Leave a comment on your pull request if you need clarification

### Stay Synced
- If someone else's changes get approved before yours, you might need to sync your fork
- Look for the "Sync fork" button and click it to get the latest version

---

## Understanding the Shop File

Think of the shop like a store with different sections:
- **Categories** = Store sections (like "Farming", "Ores", "Blocks")
- **Items** = Individual products in each section (like "Diamond", "Wheat Seeds")

### What Does the File Look Like?

Here's a simple example:

```yaml
categories:
  ores:                          # This is the section ID
    name: "&b&lOres & Ingots"   # This is what players see
    icon: "DIAMOND"              # This is the picture shown
    slot: 10                     # This is where it appears in the menu
    items:                       # Items in this section start here
      diamond:                   # This is the item ID
        type: "NORMAL"
        material: "DIAMOND"
        name: "&bDiamond"
        buy-price: 2000.0        # Players pay this to BUY
        sell-price: 15.0         # Players get this to SELL
        slot: 12
        amount: 64
```

---

## How to Change Prices

This is the most common task! Here's how:

### Example: Making Diamonds More Expensive

**Before:**
```yaml
diamond:
  type: "NORMAL"
  material: "DIAMOND"
  name: "&bDiamond"
  lore: []
  buy-price: 2000.0        # Current buy price
  sell-price: 15.0         # Current sell price
  slot: 12
  amount: 64
```

**After:**
```yaml
diamond:
  type: "NORMAL"
  material: "DIAMOND"
  name: "&bDiamond"
  lore: []
  buy-price: 3500.0        # New buy price - more expensive!
  sell-price: 20.0         # New sell price - players get more!
  slot: 12
  amount: 64
```

### Remember
- **buy-price** = What players PAY to get it from the shop
- **sell-price** = What players GET when selling to the shop
- Use `-1` for sell-price if you don't want players to sell it

### Quick Price Changes
1. Find the item in the file (use Ctrl+F to search)
2. Look for `buy-price:` or `sell-price:`
3. Change the number
4. Save (commit) your changes

---

## How to Add Color to Names

Want to make items look prettier? Use color codes!

### Simple Color Guide

Just add `&` followed by a letter before the text:

| What to Type | Color You Get |
|--------------|---------------|
| `&a` | Green |
| `&b` | Aqua (Light Blue) |
| `&c` | Red |
| `&e` | Yellow |
| `&6` | Gold/Orange |
| `&d` | Pink |
| `&5` | Purple |
| `&f` | White |
| `&l` | Make text BOLD |

### Examples You Can Copy

```yaml
name: "&aGreen Apple"         # Green colored name
name: "&bDiamond"             # Aqua/light blue
name: "&c&lREDSTONE"          # Red and bold
name: "&6Gold Ingot"          # Gold/orange color
name: "&d&lRARE ITEM"         # Pink and bold
```

### How to Use It
1. Find the `name:` line for your item
2. Add the color code right after the quote mark
3. Example: Change `name: "Diamond"` to `name: "&bDiamond"`

---

## Understanding Slots (Positions)

Slots determine where items appear in the shop menu. Think of it like a grid:

```
Row 1:   0   1   2   3   4   5   6   7   8
Row 2:   9  10  11  12  13  14  15  16  17
Row 3:  18  19  20  21  22  23  24  25  26
Row 4:  27  28  29  30  31  32  33  34  35
Row 5:  36  37  38  39  40  41  42  43  44
Row 6:  45  46  47  48  49  50  51  52  53
```

### Easy Slot Numbers to Remember
- **Top left corner** = 0
- **Top right corner** = 8
- **Middle of screen** = 22
- **Bottom left** = 45
- **Bottom right** = 53

### Tips
- Don't use the same slot number twice in the same category!
- Popular spots: 10-16, 19-25, 28-34 (the middle area)
- Leave some empty slots for a cleaner look

---

## How to Add New Items

Want to add a new item to the shop? Follow these steps:

### Step-by-Step Guide

**Step 1:** Find the category where you want to add the item
- Example: To add an item to the Farming section, search for `farming:`

**Step 2:** Scroll down to the last item in that category

**Step 3:** Copy an existing item and paste it below (keep the same spacing!)

**Step 4:** Change the details to match your new item

### Full Example: Adding Copper Ore to Ores

**Find this section:**
```yaml
  ores:
    name: "&b&lOres & Ingots"
    icon: "DIAMOND"
    slot: 10
    items:
      # ... other items here ...

      amethyst_shard:          # Last item in the list
        type: "NORMAL"
        material: "AMETHYST_SHARD"
        name: "&dAmethyst Shard"
        lore: []
        buy-price: 350.0
        sell-price: 3.5
        slot: 28
        amount: 64
```

**Add your new item below it:**
```yaml
      copper_ore:              # Your new item name (no spaces!)
        type: "NORMAL"
        material: "COPPER_ORE" # The Minecraft item name
        name: "&6Copper Ore"   # What players will see
        lore: []               # Leave empty or add description
        buy-price: 100.0       # What players pay
        sell-price: 5.0        # What players get for selling
        slot: 29               # Pick an empty slot number
        amount: 64             # How many per stack
```

### Important Tips for Adding Items
1. **Spacing matters!** Make sure your new item lines up with the others
2. **Use a unique slot number** - don't use a slot that's already taken
3. **Material names** must match Minecraft's exact names (like "DIAMOND", "IRON_ORE", "WHEAT")
4. **No spaces** in the item ID (use `copper_ore` not `copper ore`)
5. Find Minecraft material names here: https://minecraft.wiki

### Quick Copy Template

Copy this and fill in the blanks:

```yaml
      your_item_name:
        type: "NORMAL"
        material: "MATERIAL_NAME"
        name: "&fItem Display Name"
        lore: []
        buy-price: 100.0
        sell-price: 10.0
        slot: 10
        amount: 64
```

---

## Important Notes

### Price Settings
- **buy-price**: What players PAY to get the item from the shop
- **sell-price**: What players RECEIVE when selling to the shop
- Set `sell-price: -1` to disable selling (buy-only items)
- Prices are in your server's economy currency

### Material Names
- Use valid Minecraft material IDs (e.g., `DIAMOND`, `IRON_INGOT`, `OAK_LOG`)
- Material names are CASE SENSITIVE
- Find valid materials at: https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html

### Lore
- Can be empty: `lore: []`
- Or contain multiple lines:
  ```yaml
  lore:
    - "&7Line 1"
    - "&7Line 2"
    - "&aLine 3"
  ```

### Indentation
- **CRITICAL**: YAML is indentation-sensitive
- Use 2 spaces for each level of indentation
- Never use tabs
- Keep alignment consistent

### Spawners
- Only works if you have AxSpawners plugin installed
- Use `axspawner-id` to specify the mob type
- Valid mob types: zombie, skeleton, creeper, spider, enderman, blaze, etc.

### Common Mistakes
- Forgetting quotes around color codes: Use `"&bBlue"` not `&bBlue`
- Wrong indentation (use 2 spaces consistently)
- Invalid material names
- Missing required fields
- Using tabs instead of spaces
- Duplicate slot numbers (items will overlap)
- Typos in property names

---

## Common GitHub Problems & Solutions

### Problem: "I don't see a Fork button"
**Solution:** Make sure you're logged in to GitHub. Your username should appear in the top-right corner.

### Problem: "I can't find the pencil icon to edit"
**Solution:** Make sure you're in YOUR fork (it should say YourUsername/QuickkShop at the top). If you're looking at the original repository, you won't be able to edit.

### Problem: "My pull request says there are conflicts"
**Solution:** This means someone else changed the same part of the file. Click "Sync fork" on your fork's main page, then try making your changes again.

### Problem: "I committed my changes but don't see the 'Contribute' button"
**Solution:**
1. Go to the main page of YOUR fork (click "QuickkShop" at the top)
2. Look for "This branch is X commits ahead" with buttons
3. If you still don't see it, try clicking "Pull requests" at the top, then "New pull request"

### Problem: "I made a mistake in my pull request"
**Solution:**
- **Before it's approved:** Just edit the file again in your fork and commit. The changes will automatically update your pull request!
- **After it's approved:** Too late! But don't worry, you can submit a new pull request to fix it.

### Problem: "GitHub says my YAML has errors"
**Solution:**
- Check your spacing - every line should line up with similar lines
- Make sure you have quotes around item names: `"Diamond"` not `Diamond`
- Look for the line number in the error message and check that line

### Problem: "I accidentally deleted something important"
**Solution:**
1. Close your pull request (click "Close pull request" at the bottom)
2. Delete your fork (Settings → scroll to bottom → Delete this repository)
3. Start over by forking again
4. Or ask an admin for help!

---

## Need Help?

**Before asking for help, try these:**
1. Read the error message - it often tells you what's wrong and which line number
2. Check your spacing - make sure it matches other items exactly
3. Make sure you're editing YOUR fork, not the original repository
4. Double-check material names on the Minecraft wiki
5. Look at the "Common GitHub Problems" section above

**Still stuck?** Contact an admin and tell them:
- What step you're on (creating account, forking, editing, pull request, etc.)
- What you were trying to do
- What error you got (copy the exact message if there is one)
- Send a screenshot if possible!

**For YAML/config errors:**
- Check console for error messages
- Verify your YAML syntax at: https://www.yamllint.com/
- Make sure all material names are valid
- Ensure proper indentation (2 spaces per level)

---

## Tips for Success

1. **Start small** - Change one price first to learn how it works
2. **Copy existing items** - It's easier than writing from scratch
3. **Read all 6 parts** of the guide before starting
4. **Don't rush** - Take your time with each step
5. **Check the Quick Reference** at the top once you've done it once
6. **Ask questions early** - Better to ask than to submit a broken pull request!

---

**Good luck editing the shop! You've got this!**

*P.S. - GitHub might seem scary at first, but after you do it once or twice, it becomes really easy. Promise!*

---

**Last Updated**: 2025
**Plugin**: QuickkShop
