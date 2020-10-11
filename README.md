# ksWrestlingCenter

## Facebook Settings:
- *Note: Default settings applied except for the following notes.

---

### General Settings:
- Post moderation: is turned on (people can post, but admin needs to verify it before it shows up to the public)
- Post Sharing: is turned on (people can repost posts from our page)
- Photo Tagging permissions: Open to everyone (people can tag photos on our page, not just admins)
- Profanity Filter: Medium moderation

---

### Messaging Settings:
- Instant Reply turned on
 - Message: "{{user_first_name}}, thanks for reaching out! We got your message and you'll hear back from us soon."

- Away Message
 - Set to anytime outside of Normal Business Hours: M-F 7:30AM - 5:00PM
 - Message: "Hi {{user_first_name}} Thanks for reaching out! We should get back to you within the next 24-48 hours. If this is an emergency, you can reach me at {{phone_number}}."

- Automated FAQ
 - When will facility be open?
   - Response: Great question {{user_first_name}}! We will open as soon as the mats arrive  November 1st.
 - How many mats will there be?
   - Believe it or not, we will have 20 full-sized mats!

- Follow Up Messages
 - Add Follow up message when someone recommends K.W.C.
  - Message: " {{user_first_name}} that's so awesome you recommended us! We're glad you enjoyed your experience and please let us know anything that would make the experience even better."
  - Logo: the KWC logo

---

### Notifications

| Notifications                      | Status |
|:----------------------------------:|:------:|
| New Page Check-in                  | off    |
| New Page Mention                   | on     |
| New Page Review                    | on     |
| New Post Comment                   | on     |
| Edits to Comments you have written | off    |
| New Subscribers to events          | on     |
| New Followers of Page              | on     |
| New Likes on Page post             | off    |
| New Likes                          | on     |
| Edits to Posts you have written    | off    |
| New Shares on Page posts           | off    |

Alert Methods for notifications:
- Messenger : on
- Email     : off
- Text      : off

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).