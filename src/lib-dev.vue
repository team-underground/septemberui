<template>
	<div class="max-w-xl mx-auto my-12">
		<heading
			size="heading"
			class="mb-6"
		>Testing the heading</heading>
		<alert class="mb-6">Hey, this is a info alert</alert>
		<loading-button
			@click="click"
			class="mb-6"
			ref="clickButton"
		>Save Changes</loading-button>
		<date-input
			v-model="date"
			min-date="2019-12-15"
			max-date="2019-12-20"
			class="mb-6"
		></date-input>
		<div class="mb-6">
			<avatar name="Abhishek"></avatar>
		</div>
		<div class="mb-6">
			<badge>primary</badge>
		</div>
		<basic-table
			:headings="headings"
			theme="striped"
			class="mb-6"
		>
			<tr class="hover:bg-gray-100 focus-within:bg-gray-100">
				<td class="border-t">
					<span class="text-gray-700 px-6 py-4 flex items-center focus:text-indigo-500">Abhishek</span>
				</td>
				<td class="border-t">
					<span class="text-gray-700 px-6 py-4 flex items-center focus:text-indigo-500">abhisheksarmah660@gmail.com</span>
				</td>
			</tr>
			<tr class="hover:bg-gray-100 focus-within:bg-gray-100">
				<td class="border-t">
					<span class="text-gray-700 px-6 py-4 flex items-center focus:text-indigo-500">Mithicher</span>
				</td>
				<td class="border-t">
					<span class="text-gray-700 px-6 py-4 flex items-center focus:text-indigo-500">mithnehu@gmail.com</span>
				</td>
			</tr>
		</basic-table>
		<tags-input
			v-model="tags"
			label="Assign a tag"
			class="mb-6"
		></tags-input>
		<time-picker
			v-model="time"
			label="Select the time"
			class="mb-6"
		></time-picker>
		<text-input
			v-model="text"
			label="Enter your name"
			class="mb-6"
		></text-input>
		<textarea-input
			label="Add your bio"
			v-model="textarea"
			placeholder="Write something about your professional/personal career."
			class="mb-6"
		></textarea-input>
		<switch-input
			v-model="switchValue"
			color="#38C172"
			class="mb-6"
		>Approved</switch-input>
		<simple-editor
			label="Editor"
			v-model="editor"
			class="mb-6"
		></simple-editor>
		<select-input
			:options="selectOptions"
			label="Select your state"
			class="mb-6"
		></select-input>
		<search-input
			v-model="search"
			placeholder="Search by title ..."
			class="mb-6"
		></search-input>
		<radio-input
			class="mb-6"
			classes="border-2 p-3 rounded-lg"
			label="Select Gender"
			v-model="radioData"
			:options="radioOptions"
			name="gender"
			:stacked="false"
			size="large"
		>
			<template slot-scope="option">
				<div class="flex">
					<div class="pl-2 w-32">
						<h5 class="text-gray-700">{{ option.row.label }}</h5>
					</div>
				</div>
			</template>
		</radio-input>
		<link-to
			to="/"
			class="mb-6"
		>Go To Home</link-to>
		<file-input
			v-model="file"
			class="mb-6"
		></file-input>
		<div class="flex flex-end mb-6">
			<dropdown>
				<template #trigger>
					<div class="flex items-center">
						<avatar name="Abhishek Sarmah"></avatar>
						<div class="text-left ml-2">
							<span class="text-sm leading-tight block w-32 truncate">Abhishek Sarmah</span>
							<span class="leading-tight text-gray-400 block text-xs uppercase tracking-wider font-semibold">Admin</span>
						</div>
					</div>
				</template>
				<template #dropdown>
					<div class="mt-2 bg-white rounded-lg border-t border-gray-100 w-48 py-1 shadow-lg overflow-hidden">
						<a
							class="block px-4 py-2 text-gray-600 hover:bg-gray-100 hover:text-blue-600"
							href="/#"
						>Profile</a>
						<a
							class="block px-4 py-2 text-gray-600 hover:bg-gray-100 hover:text-blue-600"
							href="/#"
						>Settings</a>

						<div class="border-t my-1 border-gray-200"></div>

						<a
							class="block px-4 py-2 text-gray-600 hover:bg-gray-100 hover:text-blue-600"
							href="/#"
						>Logout</a>
					</div>
				</template>
			</dropdown>
		</div>
		<card
			with-header
			with-footer
			class="mb-6"
		>
			<template #header>
				<heading size="large">Edit Details</heading>
			</template>
			<text-input
				label="Name"
				class="mb-6"
			></text-input>
			<textarea-input label="Bio"></textarea-input>
			<template #footer>
				<loading-button size="small">Save Changes</loading-button>
			</template>
		</card>
		<accordion>
			<template #title>
				<heading size="large"> Lorem ipsum dolor sit amet.</heading>
			</template>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, pariatur doloribus officiis dolor aperiam vero nostrum alias repellat blanditiis sit?
		</accordion>
	</div>
</template>

<script>
import {
	Alert,
	DateInput,
	Heading,
	LoadingButton,
	Avatar,
	Badge,
	BasicTable,
	TagsInput,
	TimePicker,
	TextInput,
	TextareaInput,
	SwitchInput,
	SimpleEditor,
	SelectInput,
	SearchInput,
	RadioInput,
	LinkTo,
	FileInput,
	Dropdown,
	Card,
	Accordion
} from "@/entry";
export default {
	name: "SeptemberuiLibDev", // vue library dev component
	components: {
		Alert,
		DateInput,
		Heading,
		LoadingButton,
		Avatar,
		Badge,
		BasicTable,
		TagsInput,
		TimePicker,
		TextInput,
		TextareaInput,
		SwitchInput,
		SimpleEditor,
		SelectInput,
		SearchInput,
		RadioInput,
		LinkTo,
		FileInput,
		Dropdown,
		Card,
		Accordion
	},
	data() {
		return {
			date: "16/12/2019",
			headings: [
				{ title: "name", align: "left" },
				{ title: "email", align: "left" }
			],
			tags: ["book"],
			time: "12:30",
			text: null,
			textarea: null,
			switchValue: false,
			editor: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium obcaecati dolore tempore modi 
				officiis esse qui temporibus tenetur porro. Cupiditate!`,
			selectOptions: ["Assam", "Bihar", "Sikkim"],
			search: null,
			radioOptions: [
				{
					label: "Male",
					value: "Male"
				},
				{
					label: "Female",
					value: "Female"
				}
			],
			radioData: "Female",
			file: null
		};
	},
	mounted() {
		let style = document.createElement("link");
		style.type = "text/css";
		style.rel = "stylesheet";
		style.href = "https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css";
		document.head.appendChild(style);
	},
	methods: {
		click() {
			this.$refs.clickButton.startLoading();
		}
	}
};
</script> 
