# Identity Management

The identity management service is a core component to most (if not all) other Learners Guild services. It is responsible for authentication, authorization, as well as permission, role, and group management.

## Use Case Examples

### Sign-up

In order to start the culture and aptitude screenings, an Applicant is redirected to the Identity Management service service to sign-up and create a profile. She must authenticate using a Google Account and also grant read-write permissions to her Google Calendar. She must also complete any other required profile information. Once complete, she will be directed back to the Enrollment system to start the screening process.

### Authentication

A user wants to work on her next challenge, and tries to access the [Challenge Taking and Review](challenge-taking-and-review.md) service. Said user does not have a valid token to access the system, and is redirected to the Identity Management service to authenticate. User authenticates successfully using her connected Google account, then is redirected to the Challenge Taking and Review system as she initially requested.

### Authorization

A user wants to update a challenge in the curriculum, and visits the [Challenge Authoring](challenge-authoring.md) service. The challenge authoring system queries the Identity Management service to ensure appropriate permissions, passing the authentication token along with the "challenge-author" role. The given user does not have the role, so the Challenge Authoring system refuses access.

### Association

A user wants to know which other users are in her pod. From the [Group Collaboration](group-collaboration.md) service, she uses the appropriate command-line interface to list her pod-mates. The bot / webhook handling requests for that command queries the Identity Management service and renders the returned API result to the user via http response.

## Data Owned

- users
  - name
  - email address
  - password
  - physical address
  - date of birth
  - gender
  - ethnic background
  - connected 3rd-party accounts
- groups
  - group type / class (e.g., pod, cohort, etc.)
  - name
  - members (users or other groups)
- roles
  - name (e.g., partner, member, etc.)
  - members (users)
  - permissions
- permissions
  - name
  - description
