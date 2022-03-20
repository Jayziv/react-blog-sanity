# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

Following this tutorial: https://www.sanity.io/guides/build-your-first-blog-using-react
	
https://www.sanity.io/guides/build-your-first-blog-using-react#9114908f01c1
App.js wants to look like below rather than tutorial due to changes in how router works with components and elements

	// src/App.js

	import React from "react";
	import { BrowserRouter, Routes, Route } from "react-router-dom";
	import AllPosts from "./components/AllPosts.js";
	import OnePost from "./components/OnePost.js";

	function App() {
	  return (
		<BrowserRouter>
			  <div>
				  <Routes>
						<Route element={<AllPosts/>} path="/" exact />
						<Route element={<OnePost/>} path="/:slug" />
				   </Routes>
		  </div>
		</BrowserRouter>
	  );
	}
	export default App;
