# Packing page

A tap-through packing checklist in one HTML file. No server, no account, nothing to install.

Paste your list in, then walk the house one stop at a time: tap an item to move it from **to do → gathered → packed**, and long-press for **n/a**. The **Now** view shows only what you can pack right this minute: decisions first ("taking the jacket?"), then one room at a time, then whatever is waiting on something else ("after laundry").

## Use it right now

Double-click `packing.html`. It opens in your browser and asks for your list. Paste it in and hit **Save list**. That's it.

Your list and every tap are saved **in that browser on that device**. Close it, come back tomorrow, it's all still there.

## The list format

Plain lines work. Markdown works better:

```markdown
# Korea trip
Oct 24 – Nov 2

## Bathroom
- Toothbrush
- Sunscreen {order}
- Contacts {decide: wearing them this trip?}

## Closet
- Swimsuit {after: laundry}
- Jacket

## Desk
- Phone charger {day-of}
- [x] Passport

## Before leaving {todo}
- Water the plants
```

- `# Title` is the page title, and the line under it is a subtitle.
- `## Heading` is a **stop**, meaning one place in the house. The Now view opens one stop at a time and moves to the next when you finish it.
- `{decide: question}` puts the item under **Decide first**. Yes moves it into your packing; no marks it n/a.
- `{after: something}` holds the item under **Waiting on: something** until you tap "Done, unlock these". Use the same wording on every item that waits on the same thing.
- `{day-of}` is shorthand for `{after: day of}`.
- `{order}` adds an **Ordered** step for things you need to buy first.
- `- [x]` starts an item as already packed.
- `{todo}` on a heading makes that section a to-do list (tap = done) instead of packing. To-dos show under **By category**.

You can edit the list any time with **Edit list**. Items keep their status as long as you don't reword them; a reworded item starts over at "to do".

**New trip (clear statuses)** keeps the list and resets every item, ready for the next trip.

## Using it on your phone

Opening the HTML file straight from the Files app on an iPhone shows a preview that doesn't run the page, so for the phone you need the page **hosted**: served from a web address. That takes about five minutes and is free:

**Netlify Drop** is the easiest option:

1. Go to <https://app.netlify.com/drop> and sign up (free).
2. Drag the `packing-page` folder onto the page.
3. You get a web address. Open it on your phone and use Share → **Add to Home Screen**, and it behaves like an app.

**GitHub Pages** is the other good option if you already use GitHub: put `packing.html` in a repository, turn on Pages in its settings, and it is served at `https://<you>.github.io/<repo>/packing.html`.

### What hosting does and doesn't share

The hosted file is just the empty page. **Your list never goes to the host.** It's typed into your browser and stays in your browser's storage. Someone who opens your link sees a blank page that asks for their own list.

That also means **phone and laptop don't sync**: each browser has its own copy. To move a list between devices, use **Export backup** on one and **Import backup** on the other. (Syncing between devices needs a small server to hold the state. Ask Claude to build one when you want it.)

Two more things that follow from storage living in the browser:

- **Export a backup before a big trip.** Clearing your browser history or site data deletes the list, and Safari can clear data for a site you haven't opened in a few weeks. Adding the page to your Home Screen makes that much less likely.
- A private / incognito window forgets everything when you close it.

## Making it yours

It's one file, so ask Claude to change it: colours, wording, new tags, a different tap cycle. The parser and the views are commented in `packing.html`.
