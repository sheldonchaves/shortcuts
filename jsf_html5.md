#HTML5-Friendly Markup (html5 to jsf)

	//insert xmlns
	xmlns:jsf="http://xmlns.jcp.org/jsf">
#
	//div
	<div jsf:id="divid">
#
	//form
	<form jsf:id="form" jsf:prependId="false">
#
	// input
	<input type="text" jsf:id="name" placeholder="Enter name" jsf:value="#{bean.name}"/>
#
	// ajax
	<label jsf:for="name">Name </label>
	<input jsf:id="name" type="text" jsf:value="#{complex.name}">
		<f:ajax execute="@this" render="progress"/>
	</input>
#
	//progress
	<progress jsf:id="progress" max="3">#{complex.progress} of 3 </progress>
#

####Table 8-4 How Facelets Renders HTML5 Elements

HTML5 Element Name | Identifying Attribute | Facelets Tag
------------- | ------------- | -------------
a | jsf:action | h:commandLink
a | jsf:actionListener | h:commandLink
a | jsf:value | h:outputLink
a | jsf:outcome | h:link
body |  | h:body
button |  | h:commandButton
button | jsf:outcome | h:button
form |  | h:form
head |  | h:head
img |  | h:graphicImage
input | type="button" | h:commandButton
input | type="checkbox" | h:selectBooleanCheckbox
input | type="color" | h:inputText
input | type="date" | h:inputText
input | type="datetime" | h:inputText
input | type="datetime-local" | h:inputText
input | type="email" | h:inputText
input | type="month" | h:inputText
input | type="number" | h:inputText
input | type="range" | h:inputText | 
input | type="search" | h:inputText
input | type="time" | h:inputText
input | type="url" | h:inputText
input | type="week" | h:inputText
input | type="file" | h:inputFile
input | type="hidden" | h:inputHidden
input | type="password" | h:inputinput jsf:id="name" type="text" 
input | type="reset" | h:commandButton
input | type="submit" | h:commandButton
input | type="*" | h:inputText
label |  | h:outputLabel
link |  | h:outputStylesheet
script |  | h:outputScript
select | multiple="*" | h:selectManyListbox
select |  | h:selectOneListbox
textarea |  | h:inputTextArea

#Using Pass-Through Attributes (jsf with html5 props)

	//insert xmlns
	xmlns:pt="http://xmlns.jcp.org/jsf/passthrough"
#
	// input
	<h:inputText id="nights" pt:type="number" value="#{bean.nights}" pt:min="1" pt:max="30" pt:required="required" pt:title="Enter a number between 1 and 30 inclusive.">
	// render
	<input id="nights" type="number" value="1" min="1" max="30" required="required" title="Enter a number between 1 and 30 inclusive.">
#
	// f:passThroughAttribute
	<h:inputText value="#{user.email}">
		<f:passThroughAttribute name="type" value="email" />
	</h:inputText>
	// render
	<input value="me@me.com" type="email" />

####References:
https://weblogs.java.net/blog/edburns/archive/2012/11/01/html5-friendly-markup-jsf-22
#
http://blog.triadworks.com.br/suporte-a-html5-com-jsf-2-2
#
https://docs.oracle.com/javaee/7/tutorial/jsf-facelets009.htm
