<script>
	import { goto } from "$app/navigation";

	const reviews = [
		{
			text: "Всё понятно обьяснил, адекватный, быстро сработались.",
			date: "May 27, 2025",
		},
		{
			text: "на связи по вопросам постоянно, оставил на чай)",
			date: "November 4, 2025",
		},
		{
			text: "Даниэль выполнил заказ в кратчайший срок, все как оговаривали в ТЗ. Могу смело рекомендовать как ответственного и профессионального программиста. Буду сотрудничать и обращаться снова",
			date: "June 2, 2025",
		},
		{
			text: "Очень положительные впечатления от совместной работы. Высокий профессионализм и скромность.",
			date: "June 13, 2025",
		},
		{
			text: "Исключтельно положительные эмоции от сотрудничества, продолжем совместную работу",
			date: "June 14, 2025",
		},
		{
			text: "Отлично, спасибо за работу.",
			date: "June 28, 2025",
		},
		{
			text: "Хороший исполнитель, все выполнено четко по задаче.",
			date: "July 6, 2025",
		},
		{
			text: "Отличный исполнитель, сделал все быстро (для сложной задачи), приятный по общению, рекомендую",
			date: "July 26, 2025",
		},
		{
			text: "Работа выполнена на 5+, всё в срок и без нареканий. Грамотный специалист, при необходимости буду обращаться к нему снова",
			date: "October 10, 2025",
		},
		{
			text: "Отличный исполнитель, буду вновь обращаться ему",
			date: "November 4, 2025",
		},
		{
			text: "Отличный исполнитель",
			date: "October 20, 2025",
		},
		{
			text: "Работа была выполнена очень быстро, и отдельное спасибо Даниэлю за то, что он предложил альтернативное решение моей проблемы!",
			date: "September 21, 2025",
		},
		{
			text: "Хороший специалист, выполнил в срок проект, всегда был на связи, буду вновь к тебе обращаться",
			date: "October 2, 2025",
		},
		{
			text: "Отличная работа! Код написан качественно, структурированно и легко читаем. Видно, что вложено много труда и внимания к деталям, что редко получается найти у программистов. Проект работает стабильно Спасибо за профессионализм и усердие!",
			date: "October 30, 2025",
		},
	].toSorted(
		(a, b) => new Date(b.date).getTime() - new Date(a.date).getTime(),
	);
</script>

<div class="grid grid-cols-1 gap-[30px] px-5 mb-5">
	{#each reviews as r}
		<div class="w-full bg-black/20 rounded-2xl py-[13px] px-2">
			<div
				class="text-center justify-start text-gray-400 text-sm font-medium font-['Poppins'] mb-[5px]"
			>
				{r.date}
			</div>
			<div
				class="text-center justify-start text-gray-400 text-sm font-medium font-['Montserrat']"
			>
				{r.text}
			</div>
		</div>
	{/each}
</div>

<div
	class="text-center justify-start text-gray-400 text-sm font-medium font-['Poppins'] mt-[50px] mb-5"
>
	More reviews
</div>

<div class="flex gap-3.5 px-[22px]">
	<button
		onclick={() =>
			(window.location.href =
				"https://www.trustpilot.com/review/bfthdev.com")}
		class="cursor-pointer w-full py-[13px] px-[29px] text-gray-400 text-xs font-medium font-['Poppins'] bg-[#171F26] rounded-[10px] border-blue-800"
		>Trustpilot
	</button>
	<button
		onclick={() =>
			(window.location.href =
				"https://freelancehunt.com/freelancer/bibabuba.html#reviews")}
		class="cursor-pointer w-full py-[13px] px-[29px] text-gray-400 text-xs font-medium font-['Poppins'] bg-[#171F26] rounded-[10px] border-blue-800"
		>Freelancehunt
	</button>
</div>
