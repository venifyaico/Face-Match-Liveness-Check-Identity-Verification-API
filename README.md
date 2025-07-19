# Face-Match-Liveness-Check-Identity-Verification-API
This API provides advanced face recognition and liveness detection to verify user identity with a high level of security and accuracy. Whether you are building a fintech application, a biometric login system, or a KYC-compliant onboarding flow, this tool enables real-time identity verification by comparing two facial images or video against a reference image. It supports dual-verification with match score and liveness status, built for fraud prevention in industries like crypto, banking, and e-commerce. Download or clone this repo to explore the API, test endpoints using the included Postman collection (JSON file), and integrate seamlessly into your product.

<img width="1000" height="400" alt="venify_101010155" src="https://github.com/user-attachments/assets/69e916f4-57a4-4c48-bf16-b1177f8220ae" />

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
 - match_confidence (0 to 100)
 - is_match (true/false based on threshold)
   
<img width="1286" height="800" alt="venify_300148445" src="https://github.com/user-attachments/assets/9a712ae3-82bf-42f2-8d8a-c385abb6db4f" />

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
- liveness_score: 0–100

This feature is essential for detecting fraudulent account registrations and remote impersonation.

<img width="1886" height="706" alt="venify_054000126" src="https://github.com/user-attachments/assets/5f76c464-9fe5-4637-a1e7-07ce3955da3a" />


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
