<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WALL E Robotics - Building a Friend</title>
    <!-- Use Tailwind CSS for modern, responsive styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #1a202c; /* Dark background */
            color: #e2e8f0; /* Light text color */
        }
        .text-gradient {
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            background-image: linear-gradient(to right, #4F46E5, #8B5CF6); /* Original gradient */
        }
        .loading-text {
            color: #9ca3af;
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: .5; }
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header and Navigation -->
    <header class="p-6">
        <nav class="container mx-auto flex justify-between items-center">
            <div class="text-2xl font-bold">
                <a href="#" class="text-white hover:text-indigo-400 transition duration-300">WALL E Robotics</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <main class="py-16 md:py-32">
        <div class="container mx-auto px-6 text-center">
            <h1 class="text-4xl sm:text-5xl md:text-6xl font-extrabold leading-tight tracking-tight">
                <span class="text-gradient">Join us to bring WALL-E to life.</span>
            </h1>
            <p class="mt-6 text-lg sm:text-xl md:text-2xl text-gray-400 max-w-4xl mx-auto">
                We're on a quest to build a real-life WALL-E. Not just to clean up, but to find cool stuff, make friends, and probably compact some trash along the way.
            </p>
            <div class="mt-10 flex flex-col sm:flex-row justify-center items-center gap-4">
                <a href="#contact" class="px-8 py-3 bg-indigo-600 text-white font-semibold rounded-full shadow-lg hover:bg-indigo-700 transition duration-300 transform hover:scale-105">
                    I'm Ready for Adventure!
                </a>
            </div>
        </div>
        <!-- Hero Image Container -->
        <div id="hero-image-container" class="mt-16 flex justify-center px-4 min-h-[300px] md:min-h-[600px] items-center">
            <div class="loading-text text-xl">Generating WALL-E...</div>
        </div>
    </main>

    <!-- Vision Section -->
    <section class="py-16 bg-gray-800">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl font-bold mb-4">Our Quirky Vision</h2>
            <p class="text-gray-400 max-w-2xl mx-auto">
                We're building a robot with a big heart, a knack for collecting shiny things, and an even bigger talent for getting into comical situations. Because life is too short to be boring.
            </p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl font-bold">Ready to Join the Scavenger Hunt?</h2>
            <p class="mt-4 text-gray-400 max-w-xl mx-auto">
                We're looking for adventurous individuals and creative partners to help us make this vision a reality. Reach out and let's build the future together.
            </p>
            <a href="mailto:info@wallerobotics.com" class="mt-8 inline-block px-8 py-3 border border-indigo-500 text-indigo-400 font-semibold rounded-full shadow-lg hover:bg-indigo-500 hover:text-white transition duration-300 transform hover:scale-105">
                Contact Us
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-500 py-6">
        <div class="container mx-auto text-center">
            <p>&copy; 2024 WALL E Robotics. All rights reserved. (We promise to keep the sporks organized.)</p>
        </div>
    </footer>

    <script>
        // JavaScript to handle image generation and display
        window.onload = function() {
            // Function to generate an image using the AI model and inject it into a container
            async function generateImage(prompt, containerId) {
                const container = document.getElementById(containerId);
                let retryCount = 0;
                const maxRetries = 5;
                const baseDelay = 1000; // 1 second

                // Display a loading message
                container.innerHTML = '<div class="loading-text">Generating image...</div>';

                const generate = async () => {
                    const payload = {
                        instances: { prompt: prompt },
                        parameters: { "sampleCount": 1 }
                    };
                    const apiKey = "";
                    const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/imagen-3.0-generate-002:predict?key=${apiKey}`;

                    try {
                        const response = await fetch(apiUrl, {
                            method: 'POST',
                            headers: { 'Content-Type': 'application/json' },
                            body: JSON.stringify(payload)
                        });

                        if (!response.ok) {
                            if (response.status === 429 && retryCount < maxRetries) {
                                const delay = baseDelay * Math.pow(2, retryCount);
                                retryCount++;
                                await new Promise(resolve => setTimeout(resolve, delay));
                                return generate();
                            } else {
                                throw new Error(`API call failed with status: ${response.status}`);
                            }
                        }

                        const result = await response.json();
                        const base64Data = result?.predictions?.[0]?.bytesBase64Encoded;

                        if (base64Data) {
                            const imageUrl = `data:image/png;base64,${base64Data}`;
                            const imgElement = document.createElement('img');
                            imgElement.src = imageUrl;
                            imgElement.alt = prompt;
                            imgElement.className = 'w-full rounded-xl shadow-2xl transition duration-300 transform hover:scale-105';
                            container.innerHTML = '';
                            container.appendChild(imgElement);
                        } else {
                            container.innerHTML = '<div class="text-red-500">Error: Could not generate image.</div>';
                        }
                    } catch (error) {
                        console.error('Error generating image:', error);
                        container.innerHTML = `<div class="text-red-500">Error: ${error.message}. Please try again later.</div>`;
                    }
                };
                generate();
            }

            // Prompts for the AI image generation
            const heroPrompt = "a humorous, cartoon-style robot similar to WALL-E sitting on a pile of junk, looking at the stars, vibrant colors, cinematic style";
            
            // Generate images for the hero section only
            generateImage(heroPrompt, 'hero-image-container');
        };
    </script>

</body>
</html>
