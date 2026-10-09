# 5 Star Valet

A responsive business website for 5 Star Valet, designed around two customer needs: planning an event and requesting a vehicle when it is time to leave.

**[Visit the live website](https://5starvalet.netlify.app/)**

## The problem

Event organizers need to understand the service and make an inquiry. Guests at an event need a quick way to contact the valet team from their phones. The site gives each audience a clear path while presenting the business through its branding and event footage.

## The experience

- **A consistent visual identity:** black-and-gold colors, serif display typography, a looping video hero, and service sections.
- **Ticket by text:** guests can enter a ticket number to prepare a message or open a text conversation directly. They review and send the message in their messaging app.
- **Event inquiries:** a quote form collects event details and prepares a text message. Service cards preselect the relevant event type.
- **Mobile navigation:** a compact menu and persistent text/quote actions keep the main tasks within reach on smaller screens.
- **Event gallery:** videos open in a dialog and load when selected. The gallery expands to show additional footage.
- **Keyboard and screen-reader foundations:** a skip link, form labels, visible focus styles, status messages, and focus restoration after closing a video.

## How it works

The site uses **HTML, CSS, and vanilla JavaScript**. It is a static deployment on Netlify with no application server or build step. Google Fonts supplies the display and body fonts, with CSS fallback fonts available.

The ticket and quote flows use `sms:` links with encoded message text. JavaScript handles mobile navigation, form validation, gallery playback, and copy-message alternatives.

This version does **not** send messages automatically, save inquiries, confirm bookings, or dispatch vehicles. The customer must press **Send** in their messaging app, and the valet team handles the request. No conversion or wait-time improvements have been measured or claimed.

## Run locally

Clone or download this repository, then open a terminal in its folder:

```sh
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Python 3 is the only requirement for this local preview; there are no npm packages to install. Stop the server with `Ctrl+C`.

```text
index.html       Page structure and content
styles.css       Visual design and responsive layouts
script.js        Navigation, gallery, and SMS handoffs
assets/          Brand images, photographs, and event videos
```

## Verification and next steps

The live desktop page and source have been reviewed. Before making broader accessibility or device-compatibility claims, verify the mobile menu, keyboard navigation, form errors, gallery dialog, and SMS message preparation on actual iOS and Android devices. Opening a prepared message is sufficient for testing; a message does not need to be sent.

The background video currently loops without a pause control. The reduced-motion CSS disables interface transitions, but does not stop that video. A motion-control option and a complete accessibility review are useful next improvements.

## Project attribution

Project owner: **Yahya Vaid**. Developed iteratively with ChatGPT/Codex assistance for design, implementation, and documentation, guided by the business requirements and feedback.

Branding, photographs, and videos remain the property of their respective rights holders. They are included for this project; repository visibility does not grant permission to reuse them. No open-source license has been assigned to this repository.
