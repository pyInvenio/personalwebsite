<script>
	import Icon from '@iconify/svelte';
</script>

<div class="relative mx-auto flex  lg:w-[50%] w-[95%] flex-col justify-center my-8 z-10">
	<div class="w-full flex flex-col md:flex-row items-center">
		<div class="flex flex-col w-full lg:mr-0 mx-8 md:mt-0 mt-8">
			<h1 class="text-3xl mb-4">CoViLa</h1>
			<h3 class="text-xl italic">Computer Vision Ball Launcher</h3>
			<div class="my-4">
				<img src="/hardtech/covilaskate.jpg" alt="" class=" mx-auto" />Imagine a world where you can
				play fetch with your dog without having to throw the ball. Or where you can train for a
				sport without needing a throwing partner. That is where CoViLa's inspiration came to be.
				<br /><br />
				As part of my TJ senior research project, I worked on the development of the autonomous human
				identifier and tracker, as well as the motor control for the ball launcher. <br /><br />
				<h1>CV</h1>
				Fast, real-time CV was a challenge for this project, as we were running fairly low compute
				powere on a Raspberry Pi 4. Therefore, I used OpenCV haar-cascades for realtime torso
				detection. I also used OpenCV for identifying a person through centroids. This allowed the
				system to track a person, be robust to possible noise and occlusion, and be able to identify
				a person even if they were not facing the camera.<br />To be able to estimate the distance
				of the person from the camera, I used a stereo camera setup and the library StereoVision.
				This allowed me to estimate the distance of the person from the camera, and therefore the
				angle at which the ball should be launched.
				<br /><br />
				<h1>Robot</h1>
				The robot was modeled in Autodesk Fusion and built using 80x20 aluminum extrusion with a
				spinning jenny for free rotation. The robot was controlled using a Raspberry Pi 4 and a
				L298N motor driver. With a high RPM motor, we created a 3D printed flywheel that could
				launch a ball at a speed of 20mph. We got the robot to effectively move, track a person, and
				launch a ball. However, one oversight we had was that the flywheel would get very hot.
				Eventually, the wheel melted and the motor burned out.<iframe
					src="https://drive.google.com/file/d/1JJK_mDchtpIRAuP8Y-i79m4zjK38XgG3/preview"
					class="w-full  aspect-video md:h-96 h-64 my-2"
					frameborder="0"
					allowfullscreen
					allow="autoplay"
					title="CoViLa"
				/>
			</div>
		</div>
	</div>
</div>

<style type="scss">
	img {
		@apply mx-auto max-h-64 my-4;
	}
	h1 {
		@apply text-2xl;
	}
</style>
