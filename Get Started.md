
## Getting Started In MassEnergize As A Frontend Developer
On this board, you will find all the necessary information needed to get started as a developer with making changes and building on anything on the **MassEnergize**
user portal **(Made with React)**. This board will give directions to very tricky, and important files as well as details that make up the core functionality of the whole site. 
<br/> Mind you, the information here is in no way going to take anyone through a **React**, it is just to document the structure of everything, where to find core files,
and simple instructions to how to use custom components that have been created.

### TABLE OF CONTENT 
* <a href="#file-to-page"> Which files show what page?  </a>
* <a href="#setting-your-env"> Configuring your working environment (is_prod,is_local,is_canary, is_dev, is_sandbox) </a>
* <a href="#developer-workflow"> ME developer workflow and push protocol</a>
* <a href="#"> Want to know how ME custom components work? </a>
* <a href="#"> Want to know how each ME page works? </a>



#### <a name="file-to-page">WHICH FILES SHOW WHAT PAGE </a>
 **Page** | **Related Files** 
 ---------| ----------------- 
<a href="https://community-dev.massenergize.org/">Community Selection Page</a> | `CommunitySelectPage.js`
<a href="https://community-dev.massenergize.org/wayland/">Homepage</a> | `Homepage.js`, `WelcomeImages.js`, `IconBoxTable.js`, `EventHomepageSection.js`
<a href="https://community-dev.massenergize.org/wayland/actions">All Actions Page</a> | `ActionsPage.js`, `Cart.js`, `Funnel.js`
<a href="https://community-dev.massenergize.org/wayland/actions">Action Cards On Actions Page</a> | `PhotoSensitiveAction.js` `ChooseHHForm.js`
<a href="https://community-dev.massenergize.org/wayland/actions" target="_blank">Individual Action Page</a> | `OneActionPage.js` `ChooseHHForm.js`, `StoryForm.js`, `Cart.js`
<a href="https://community-dev.massenergize.org/wayland/teams">All Teams Page</a> | `TeamsPage.js`, `TeamsInfoModal.js` `TeamsStatsBars.js`
<a href="https://community-dev.massenergize.org/wayland/teams">One Team</a> | `TeamsInfoModal.js`, `TeamsStatsBars.js`, `MEModal.js`
<a href="https://community-dev.massenergize.org/wayland/services">All Service Providers</a> | `ServicesPage.js`, `Funnel.js`
<a href="https://community-dev.massenergize.org/wayland/services">One Service Provider</a> | `ServicesPage.js`
<a href="https://community-dev.massenergize.org/wayland/testimonials">All Testimonials Page</a> | `StoriesPage.js`, `StoryForm.js`, `Funnel.js`, `METestimonialCard.js`
<a href="https://community-dev.massenergize.org/wayland/testimonials">One Testimonial Page</a> | `OneTestimonialPage.js`
<a href="https://community-dev.massenergize.org/wayland/events">All Events Page</a> | `EventsPageReal.js`, `NewEventsCard.js`
<a href="https://community-dev.massenergize.org/wayland/events">One Event Page</a> | `OneEventPage.js`
<a href="https://community-dev.massenergize.org/wayland/impact">Our Impact Page</a> | `impactPage.js`, `Utils.js`
<a href="https://community-dev.massenergize.org/wayland/aboutus">About Us Page</a> | `AboutUsPage.js`
<a href="https://community-dev.massenergize.org/wayland/donate">Donate Page</a> | `DonatePage.js`
<a href="https://community-dev.massenergize.org/wayland/donate">Contact Us Page</a> | `ContactUsPage.js`, `ContactPageForm.js`
<a href="https://community-dev.massenergize.org/wayland/signin">Login Page </a> | `LoginPage.js`, `LoginForm.js`
<a href="https://community-dev.massenergize.org/wayland/signup">Registration Page </a> | `RegistrationPage.js`, `RegistrationForm.js`
<a href="#">All Redux Actions </a> | `userActions.js`, `pageActions.js`, `linkActions.js`
<a href="#">All Redux Reducers </a> | `reducers/index.js`, `linkReducer.js`, `pageReducer.js`, `userReducer.js`
<a href="#">Most Configuration Files </a> | `config.json`, `firebaseConfig.js`, `config/index.js`
<br/>

### <a name="setting-your-env">CONFIGURING YOUR WORKING ENVIRONMENT </a>
At the time of writing, there are **five** working environments available in MassEnergize. These environments dictate the the kind of data you have access to, and interact with from the backend. You are free to tweak your configuration settings and interact with the data as you wish. <br/>
**_However, please note that PROD, and CANARY, are not your playground. You may switch to them ONLY to view how real data may look with any new changes you might have made; for all other tests, thats what local and dev modes are for!_**<br/>
#### How do I switch?
Easy! kindly move into your `/config/config.json` file and make changes to the bolean values that correspond to the environment you would like to working in. The various combinations that create the working environments are as follows. 

Environment |IS_LOCAL |IS_PROD|IS_SANDBOX|IS_CANARY|
------------|---------|-------|----------|---------|
Development| `false` | `false`| `false` | `false`
Production | `false`| `true` | `false` | `false`
Canary | `false` | `false` | `false`|`true` 
Sandbox | `false` | `false` | `true`| `false` 
Local | `true` | `false` | `false` | `false`

Dont get excited yet. Before you switch to local and expect magic to happen, 
make sure you have followed <a href="https://massenergize.slite.com/p/note/KWfwNLonZsf4bfGD6CNcJq">this link on how to setup your local backend on ME </a><br/>
The other environments do not need any setup :fire:. <br/>However, due to a recent change in our authentication system, you may not be able to send data to the backend because of token issues. You should set your environment up locally.

### <a name="#developer-workflow">DEVELOPER WORKFLOW AND PUSH PROTOCOL  </a>
If you have not been assigned a ticket yet, enjoy your leisure moments as best you can, Kaat is probably creating a ticket for you as you read :rofl:. You will be assigned soon.
When you are assigned, here  are a few things to note.

**Slack Workflow Notification**<br/>
Before you get started with any assigned tickets on github, or just randomly fixing non-ticketed bugs, notify the team! 
Use the **team_updates** channel to do this. 
Use the bolt icon <br/>
<img src="./images/bolt.png"/><br/>
Then select **Daily Standup** from the options as shown<br/>
<img src="./images/standup.png"/><br/> 
Now fill the form appropriately with what you have been up to, and what you intend to tackle, then submit. 
<img src="./images/standup-form.png" />

... to be continued






