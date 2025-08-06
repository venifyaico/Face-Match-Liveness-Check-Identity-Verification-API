# Face-Match-Liveness-Check-Identity-Verification-API
This API provides advanced face recognition and liveness detection to verify user identity with a high level of security and accuracy. Whether you are building a fintech application, a biometric login system, or a KYC-compliant onboarding flow, this tool enables real-time identity verification by comparing two facial images or video against a reference image. 

Download or clone this repo to explore the API, test endpoints using the included Postman collection (JSON file), and integrate seamlessly into your product.


![photo-2025-07-22-05-00-05 (1)](https://github.com/user-attachments/assets/75e1130a-4a2b-401f-bea1-877b579a6040)

## Why Choose This API?
The Venify Face Match & Liveness Check API is built for security-first applications in industries like fintech, healthcare, e-learning, and on-demand services. Whether you're creating a banking login system, a digital identity check, or a secure sign-up flow, this API enables quick and precise biometric analysis.

### Key Benefits
  - Face Match Score: Compares two faces and returns a similarity score (0–100)
  - Liveness Detection: Verifies that the face is real and not from a static or spoofed source
  - AI-Powered Deep Learning Models: Trained on diverse datasets for bias-resistant predictions
  - Fast & Scalable: Average response time under 2 seconds
  - Flexible Input: Accepts images in base64 or direct file upload
  - Developer Dashboard & Logs: Track usage and debug with ease on RapidAPI

---

## How to Get Started
 1. Go to the API page on [RapidAPI](https://rapidapi.com/venify-venify-default/api/face-match-liveness-check-identity-verification)
 2. Subscribe with a free or paid plan
 3. Test the API directly in-browser
 4. Integrate into your backend in Python, JavaScript, PHP, or any HTTP client

### Postman Collection
This Postman collection includes ready-to-use requests:

**How to Use**
 1. Download [the collection JSON](./FaceMatch_VideoLiveness.postman_collection.json) or clone this repo
 2. Open Postman and click “Import”.
 3. Select the file: **FaceMatch_VideoLiveness.postman_collection.json**
 4. Add your RapidAPI key in the headers or use an environment variable.
 5. Start sending requests and previewing image responses.

## API Features

### 1. Face Match
Compare two faces — usually a selfie and a photo ID image — to confirm if they belong to the same person.

crop_face_2: Set to 1 to receive a cropped version of the detected face from image_2 in base64. Useful if you want to display the face preview in your UI or store it for logs. Set to 0 to disable.

**Returns:**
 - is_match (true/false based on threshold)
   
<img width="1280" height="490" alt="paper-attack" src="https://github.com/user-attachments/assets/30c66930-eeda-4cb5-8818-c7661fe6cea2" />


<br/>
<br/>
<br/>

```bash
curl --request POST 
	--url https://face-match-liveness-check-identity-verification.p.rapidapi.com/api/v1/compare_faces 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: face-match-liveness-check-identity-verification.p.rapidapi.com' 
	--header 'x-rapidapi-key: YOUR_RAPIDAPI_KEY' 
	--form image_1=image1.jpg 
	--form image_2=image2.jpg 
	--form crop_face_2=0
 ```

### 2. Liveness Detection
Analyzes the live selfie to detect signs of spoofing:
 - Is the image from a screen or printed photo?
 - Is it a deepfake?
 - Are there signs of human skin tone, 3D depth, and motion?

**Returns:**
- is_live_face: true or false

This feature is essential for detecting fraudulent account registrations and remote impersonation.


<img width="1280" height="298" alt="paper-attack (1)" src="https://github.com/user-attachments/assets/ba7d1c38-6158-4fac-a06c-d5bc4c8008dd" />


<br/>
<br/>
<br/>

```bash
curl --request POST 
	--url https://face-match-liveness-check-identity-verification.p.rapidapi.com/api/v1/video_authentication 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: face-match-liveness-check-identity-verification.p.rapidapi.com' 
	--header 'x-rapidapi-key: YOUR_RAPIDAPI_KEY' 
	--form 'image=image.jpg' 
	--form 'video=video.mkv'
```

## Use Cases

 - Fintech Onboarding: Seamless user verification in seconds
 - Banking & Finance: Prevent account takeovers with biometric security
 - e-KYC/AML Compliance: Ensure regulatory compliance for remote verification
 - Telemedicine: Verify identity for patient data protection
 - Online Education: Prevent exam fraud and ensure student authenticity
 - Marketplace & Sharing Apps: Verify seller and buyer identities

## License
This API is provided by [Venify on RapidAPI](https://rapidapi.com/venify-venify-default/api/face-match-liveness-check-identity-verification). Please refer to their usage terms, pricing, and limits.
