/* ---------- Content (edit everything here) ---------- */
const CONFIG = {
  contactName: "Colleague",
  contactRole: "Team member",
  appName: "Messages",
  notificationText: "You have a new message from your colleague.",
  practiceNotice: "This is a practice conversation for self-assessment. Always follow your organisation's procedures.",
  greeting: "Hi! I'd like to talk through a few work situations with you. I'd value your perspective.",
  greetingAgain: "Hi again! Let's go through these situations one more time.",
  closing: "Thanks for sharing your thoughts! Talking these situations through helps us all work safely and consistently."
};

const GREETING = CONFIG.greeting;
const GREETING_AGAIN = CONFIG.greetingAgain;
const CLOSING = CONFIG.closing;

const questions = [
  {
    question: "Here's the first situation: [describe the situation]. What do you think we should do?",
    options: [
      "[Recommended action]",
      "[Alternative action]",
      "[Less suitable action]"
    ],
    responses: [
      "Exactly! [Explain why this is the right approach.]",
      "That's worth considering. [Explain what should come first or what's missing.]",
      "I see why you'd think that, but [explain the risk and the better approach]."
    ]
  },
  {
    question: "Let's look at another situation: [describe the situation]. What would you do?",
    options: [
      "[Recommended action]",
      "[Alternative action]",
      "[Less suitable action]"
    ],
    responses: [
      "Great choice! [Explain why this is the right approach.]",
      "Good thinking. [Explain how to build on this choice.]",
      "Let's be careful here. [Explain the risk and the better approach.]"
    ]
  },
  {
    question: "One last situation: [describe the situation]. How should we handle it?",
    options: [
      "[Recommended action]",
      "[Alternative action]",
      "[Less suitable action]"
    ],
    responses: [
      "I agree! [Explain why this is the right approach.]",
      "That's a useful step. [Explain what else needs to happen.]",
      "Let's avoid that. [Explain why and what the correct procedure is.]"
    ]
  }
];

/* Apply names and labels to the page */
document.title = CONFIG.contactName;
document.querySelector(".notif-title").textContent = CONFIG.contactName;
document.querySelector(".notif-text").textContent = CONFIG.notificationText;
document.querySelector(".notif-top span").textContent = CONFIG.appName;
document.querySelector(".who .name").textContent = CONFIG.contactName;
document.getElementById("status").textContent = CONFIG.contactRole;
document.getElementById("notif").setAttribute("aria-label", "Open message from " + CONFIG.contactName);
