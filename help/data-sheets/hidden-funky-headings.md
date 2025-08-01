---
title: Bibliothèques de balises
description: Les bibliothèques de balises Granite, CQ et Sling vous donnent accès à des fonctions spécifiques à utiliser dans le script JSP de vos modèles et composants
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.5/SITES
topic-tags: platform
content-type: reference
solution: Experience Manager, Experience Manager Sites
hide: true
hidefromtoc: true
role: Developer
exl-id: d024b7e9-1e8e-4aa3-bbb8-7bc92d143a1f
source-git-commit: 80a9777d6ad45894a1257a62f50b3d232f39aed9
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 0%

---

# Bibliothèques de balises{#tag-libraries}

Les bibliothèques de balises Granite, CQ et Sling vous donnent accès à des fonctions spécifiques à utiliser dans le script JSP de vos modèles et composants.

## **Titre en gras**

Il s’agit d’un titre en gras ci-dessus.

1Er Août 2025

## *En-tête en italique*

Il s&#39;agit d&#39;un titre en italique ci-dessus.

## Bibliothèque de balises Granite {#granite-tag-library}

La bibliothèque de balises Granite contient des fonctions utiles.

Lorsque vous développez le script jsp d’un composant de l’IU Granite, il est recommandé d’inclure le code suivant en haut du script :

```xml
<%@include file="/libs/granite/ui/global.jsp"%>
```

Le global déclare également la bibliothèque Sling.

```xml
<%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling" %>
```

### &lt;ui:includeClientLib> {#ui-includeclientlib}

La balise `<ui:includeClientLib>` comprend une bibliothèque cliente HTML AEM, qui peut être de type js, css ou theme. Pour plusieurs inclusions de types différents (js et css, par exemple), cette balise doit être utilisée plusieurs fois dans le fichier jsp. Cette balise est un wrapper pratique qui entoure l’interface de service ` [com.adobe.granite.ui.clientlibs.HtmlLibraryManager](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/javadoc/com/adobe/granite/ui/clientlibs/HtmlLibraryManager.html)`.

Il possède les attributs suivants :

**categories** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques JavaScript et CSS pour les catégories données. Le nom du thème est extrait de la requête.

Équivalent à : `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeIncludes`

**theme** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques liées au thème (à la fois CSS et JS) pour les catégories données. Le nom du thème est extrait de la requête.

Équivalent à : `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeThemeInclude`

**js** - Liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques JavaScript pour les catégories données.

Équivalent à : `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeJsInclude`

**css** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques CSS pour les catégories données.

Équivalent à : `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeCssInclude`

**themed** - Un indicateur qui signale que seules les bibliothèques avec thème ou sans thème doivent être incluses. Si cet attribut est omis, les deux ensembles sont inclus. S’applique uniquement aux inclusions JS ou CSS pures (et non aux catégories ou aux inclusions de thème).

La balise `<ui:includeClientLib>` peut être utilisée comme suit dans un fichier jsp :

```xml
<%-- all: js + theme (theme-js + css) --%>
<ui:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<ui:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<ui:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<ui:includeClientLib css="cq.collab.calendar, cq.security" />
```

## Bibliothèque de balises CQ {#cq-tag-library}

La bibliothèque de balises CQ contient des fonctions utiles.

Pour utiliser la bibliothèque de balises CQ dans votre script, celui-ci doit commencer par le code suivant :

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %>
```

>[!NOTE]
>
>Lorsque le fichier `/libs/foundation/global.jsp` est inclus dans le script, la bibliothèque de balises est automatiquement déclarée.

Lorsque vous développez le script jsp d’un composant AEM, il est recommandé d’inclure le code suivant en haut du script :

```xml
<%@include file="/libs/foundation/global.jsp"%>
```

Il déclare les bibliothèques de balises sling, CQ et jstl, et expose les objets de script utilisés régulièrement par la balise [`<cq:defineObjects />`](#amp-lt-cq-defineobjects). Cela raccourcit et simplifie le code jsp de votre composant.

### &lt;cq:text> {#cq-text}

La balise `<cq:text>` est une balise pratique qui génère le texte du composant dans un JSP.

Il présente les attributs facultatifs suivants :

**property** - Nom de la propriété à utiliser. Le nom est relatif à la ressource actuelle.

**value** - Valeur à utiliser pour la sortie. Si cet attribut est présent, il remplace l’utilisation de l’attribut property.

**oldValue** - Valeur à utiliser pour la sortie diff. Si cet attribut est présent, il remplace l’utilisation de l’attribut property.

**escapeXml** - Définit si les caractères &lt;, >, &amp;, ’ et «  figurant dans la chaîne obtenue doivent être convertis en codes d’entité de caractères correspondants. La valeur par défaut est false. L’échappement est appliqué après la mise en forme facultative.

**format** - java.text.Format facultatif à utiliser pour la mise en forme du texte.

**noDiff** - Supprime le calcul d’une sortie diff, même si des informations diff sont présentes.

**tagClass** - Nom de classe CSS d’un élément qui entoure une sortie non vide. Si vide, aucun élément n’est ajouté.

**tagName** - Nom de l’élément qui entoure une sortie non vide. La valeur par défaut est DIV.

**placeholder** - Valeur par défaut à utiliser pour le texte nul ou vide en mode d’édition, c’est-à-dire l’espace réservé. La vérification par défaut est effectuée après l’échappement et la mise en forme facultatifs ; en d’autres termes, elle est écrite telle quelle dans la sortie. La valeur par défaut est :

`<div><span class="cq-text-placeholder">&para;</span></div>`

**default** - Valeur par défaut à utiliser pour le texte nul ou vide. La vérification par défaut est effectuée après l’échappement et la mise en forme facultatifs ; en d’autres termes, elle est écrite telle quelle dans la sortie.

Voici quelques exemples d’utilisation de la balise `<cq:text>` dans un JSP :

```xml
<cq:text property="jcr:title" tagName="h2"/>
<cq:text property="jcr:description" tagName="p"/>

<cq:text value="<%= listItem.getTitle() %>" tagName="h4" placeholder="" />
<cq:text value="<%= listItem.getDescription() %>" tagName="p" placeholder=""/>

<cq:text property="jcr:title" value="<%= title %>" tagName="h3"/><%
    } else if (type.equals("link")) {
        %><cq:text property="jcr:title" value="<%= "\u00bb " + title %>" tagName="p" tagClass="link"/><%
    } else if (type.equals("extralarge")) {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h1"/><%
    } else {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h2"/><%

<cq:text property="jcr:description" placeholder="" tagName="small"/>

<cq:text property="tableData"
               escapeXml="false"
               placeholder="<img src=\"/libs/cq/ui/resources/0.gif\" class=\"cq-table-placeholder\" alt=\"\">"
    />

<cq:text property="text"/>

<cq:text property="image/jcr:description" placeholder="" tagName="small"/>
<cq:text property="text" tagClass="text"/>
```

### &lt;cq:setContentBundle> {#cq-setcontentbundle}

La balise `<cq:setContentBundle>` crée un contexte de localisation i18n et le stocke dans la variable de configuration `javax.servlet.jsp.jstl.fmt.localizationContext`.

Il possède les attributs suivants :

**language** - La langue du paramètre régional pour lequel le lot de ressources doit être récupéré.

**source** - Source où le paramètre régional doit être pris. Elle peut être définie sur l’une des valeurs suivantes :

* **static** - Le paramètre régional provient de l’attribut `language`, s’il est disponible ; dans le cas contraire, il provient du paramètre régional par défaut du serveur.

* **page** - Le paramètre régional provient de la langue de la page ou de la ressource en cours, si elle est disponible, sinon de l’attribut `language`, si elle est disponible, sinon du paramètre régional par défaut du serveur.

* **request** - Le paramètre régional provient du paramètre régional de la requête ( `request.getLocale()`).

* **auto** - Le paramètre régional provient de l’attribut `language`, s’il est disponible, sinon de la page ou de la ressource en cours, si elle est disponible ; si elle ne l’est pas, il est extrait de la requête.

Si l’attribut `source` n’est pas défini :

* Si l’attribut `language` est défini, l’attribut `source` est défini par défaut sur « `static`.

* Si l’attribut `language` n’est pas défini, l’attribut `source` est défini par défaut sur `auto`.

Le « lot de contenu » peut être utilisé par des balises `<fmt:message>` JSTL standard. La recherche de messages par clés se divise en deux parties :

1. Tout d’abord, les propriétés JCR de la ressource sous-jacente générée sont recherchées pour les traductions. Vous pouvez ainsi définir une boîte de dialogue de composant simple pour modifier ces valeurs.
1. Si le nœud ne contient pas de propriété dont le nom correspond exactement à celui de la clé, la solution de secours consiste à charger un lot de ressources à partir de la requête sling ( `SlingHttpServletRequest.getResourceBundle(Locale)`). La langue ou le paramètre régional de ce lot est défini par les attributs de langue et source de la balise `<cq:setContentBundle>` .

La balise `<cq:setContentBundle>` peut être utilisée comme suit dans un fichier jsp :

Pour les pages qui définissent leur langue :

```xml
... %><cq:setContentBundle source="page"/><%  %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

Pour les pages personnalisées par l’utilisateur :

```xml
... %><cq:setContentBundle scope="request"/><% %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

### &lt;cq:include> {#cq-include}

La balise `<cq:include>` inclut une ressource dans la page active.

Il possède les attributs suivants :

**flush**

* Valeur booléenne définissant s’il faut vider la sortie avant d’inclure la cible.

**chemin**

* Chemin d’accès à l’objet de ressource à inclure dans le traitement de la requête en cours. Si ce chemin d’accès est relatif, il est ajouté au chemin d’accès de la ressource actuelle dont le script inclut la ressource donnée. Les attributs path et resourceType ou script doivent être spécifiés.

**resourceType**

* Type de ressource de la ressource à inclure. Si le type de ressource est défini, le chemin doit être le chemin exact vers un objet de ressource : dans ce cas, l’ajout de paramètres, de sélecteurs et d’extensions au chemin n’est pas pris en charge.
* Si la ressource à inclure est spécifiée avec l’attribut path qui ne peut pas être résolu en ressource, la balise peut créer un objet de ressource de synthèse en dehors du chemin et de ce type de ressource.
* Les attributs path et resourceType ou script doivent être spécifiés.

**script**

* Script jsp à inclure. Les attributs path et resourceType ou script doivent être spécifiés.

**ignoreComponentHierarchy**

* Valeur booléenne contrôlant si la hiérarchie de composant doit être ignorée pour la résolution du script. Si la valeur est true, seuls les chemins de recherche sont respectés.

**Exemple :**

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><div class="center">
    <cq:include path="trail" resourceType="foundation/components/breadcrumb" />
    <cq:include path="title" resourceType="foundation/components/title" />
    <cq:include script="redirect.jsp"/>
    <cq:include path="par" resourceType="foundation/components/parsys" />
</div>
```

Devriez-vous utiliser `<%@ include file="myScript.jsp" %>` ou `<cq:include script="myScript.jsp" %>` pour inclure un script ?

* La directive `<%@ include file="myScript.jsp" %>` informe le compilateur JSP d’inclure un fichier complet dans le fichier actuel. C’est comme si le contenu du fichier inclus était collé directement dans le fichier d’origine.
* Avec la balise `<cq:include script="myScript.jsp">`, le fichier est inclus au moment de l’exécution.

Devriez-vous utiliser `<cq:include>` ou `<sling:include>` ?

* Lors du développement de composants AEM, Adobe vous recommande d’utiliser `<cq:include>`.
* `<cq:include>` vous permet d’inclure directement des fichiers de script en fonction de leur nom lors de l’utilisation de l’attribut script. Cela prend en compte l’héritage du type de composant et de ressource et est souvent plus simple que le strict respect de la résolution de script de Sling à l’aide de sélecteurs et d’extensions.

### &lt;cq:includeClientLib> {#cq-includeclientlib}

>[!CAUTION]
>
>`<cq:includeClientLib>` obsolète depuis AEM 5.6. `<ui:includeClientLib>` doit être utilisé à la place.

La balise `<cq:includeClientLib>` comprend une bibliothèque cliente HTML AEM, qui peut être de type js, css ou theme. Pour plusieurs inclusions de types différents (js et css, par exemple), cette balise doit être utilisée plusieurs fois dans le fichier jsp. Cette balise est un wrapper pratique qui entoure l’interface de service `com.day.cq.widget.HtmlLibraryManager`.

Il possède les attributs suivants :

**categories** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques JavaScript et CSS pour les catégories données. Le nom du thème est extrait de la requête.

Équivalent à : `com.day.cq.widget.HtmlLibraryManager#writeIncludes`

**theme** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques liées au thème (à la fois CSS et JS) pour les catégories données. Le nom du thème est extrait de la requête.

Équivalent à : `com.day.cq.widget.HtmlLibraryManager#`writeThemeInclude

**js** - Liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques JavaScript pour les catégories données.

Équivalent à : `com.day.cq.widget.HtmlLibraryManager#writeJsInclude`

**css** - Une liste de catégories de bibliothèques clientes séparées par des virgules. Cela inclut toutes les bibliothèques CSS pour les catégories données.

Équivalent à : `com.day.cq.widget.HtmlLibraryManager#writeCssInclude`

**themed** - Un indicateur qui signale que seules les bibliothèques avec thème ou sans thème doivent être incluses. Si cet attribut est omis, les deux ensembles sont inclus. S’applique uniquement aux inclusions JS ou CSS pures (et non aux catégories ou aux inclusions de thème).

La balise `<cq:includeClientLib>` peut être utilisée comme suit dans un fichier jsp :

```xml
<%-- all: js + theme (theme-js + css) --%>
<cq:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<cq:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<cq:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<cq:includeClientLib css="cq.collab.calendar, cq.security" />
```

### &lt;cq:defineObjects> {#cq-defineobjects}

La balise `<cq:defineObjects>` expose les objets de script suivants, utilisés régulièrement, qui peuvent être référencés par le développeur. Elle expose également les objets définis par la balise [`<sling:defineObjects>`](#amp-lt-sling-defineobjects).

**componentContext**

* l’objet de contexte de composant actuel de la requête (interface com.day.cq.wcm.api.components.ComponentContext).

**composant**

* l’objet du composant AEM actif de la ressource active (interface com.day.cq.wcm.api.components.Component).

**currentDesign**

* l’objet de conception actif de la page active (interface com.day.cq.wcm.api.designer.Design).

**currentPage**

* l’objet de page de gestion de contenu web AEM actif (interface com.day.cq.wcm.api.Page).

**currentStyle**

* Objet de style actuel de la cellule active (interface com.day.cq.wcm.api.designer.Style).

**designer**

* objet designer utilisé pour accéder aux informations de conception (interface com.day.cq.wcm.api.designer.Designer).

**editContext**

* l’objet editContext du composant AEM (interface com.day.cq.wcm.api.components.EditContext).

**pageManager**

* Objet de gestionnaire de page pour les opérations au niveau de la page (interface com.day.cq.wcm.api.PageManager).

**pageProperties**

* Objet des propriétés de la page active (org.apache.sling.api.resource.ValueMap).

**propriétés**

* Objet de propriétés de la ressource active (org.apache.sling.api.resource.ValueMap).

**resourceDesign**

* l’objet de conception de la page de ressource (interface com.day.cq.wcm.api.designer.Design).

**resourcePage**

* l’objet de page de ressource (interface com.day.cq.wcm.api.Page).
* Il possède les attributs suivants :

**requestName**

* hérité de sling

**responseName**

* hérité de sling

**resourceName**

* hérité de sling

**nodeName**

* hérité de sling

**logName**

* hérité de sling

**resourceResolverName**

* hérité de sling

**slingName**

* hérité de sling

**componentContextName**

* spécifique à la gestion de contenu web

**editContextName**

* spécifique à la gestion de contenu web

**propertiesName**

* spécifique à la gestion de contenu web

**pageManagerName**

* spécifique à la gestion de contenu web

**currentPageName**

* spécifique à la gestion de contenu web

**resourcePageName**

* spécifique à la gestion de contenu web

**pagePropertiesName**

* spécifique à la gestion de contenu web

**componentName**

* spécifique à la gestion de contenu web

**designerName**

* spécifique à la gestion de contenu web

**currentDesignName**

* spécifique à la gestion de contenu web

**resourceDesignName**

* spécifique à la gestion de contenu web

**currentStyleName**

* spécifique à la gestion de contenu web

**Exemple**

```xml
<%@page session="false" contentType="text/html; charset=utf-8" %><%
%><%@ page import="com.day.cq.wcm.api.WCMMode" %><%
%><%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><cq:defineObjects/>
```

>[!NOTE]
>
>Lorsque le fichier `/libs/foundation/global.jsp` est inclus dans le script, la balise `<cq:defineObjects />` est automatiquement incluse.

### &lt;cq:requestURL> {#cq-requesturl}

La balise `<cq:requestURL>` écrit l’URL de requête en cours dans JspWriter. Les deux balises [`<cq:addParam>`](#amp-lt-cq-addparam) et [`<cq:removeParam>`](#amp-lt-cq-removeparam) et peuvent être utilisées dans le corps de cette balise pour modifier l’URL de requête actuelle avant qu’elle ne soit écrite.

Il permet de créer des liens vers la page active avec des paramètres variables. Elle permet, par exemple, de transformer la requête :

`mypage.html?mode=view&query=something` en `mypage.html?query=something`.

L’utilisation de `addParam` ou `removeParam` ne modifie que l’occurrence du paramètre donné ; aucun autre paramètre n’est affecté.

`<cq:requestURL>` n’a aucun attribut.

Exemples :

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:addParam> {#cq-addparam}

La balise `<cq:addParam>` ajoute un paramètre de requête avec le nom et la valeur spécifiés à la balise [`<cq:requestURL>`](#amp-lt-cq-requesturl) englobante.

Il possède les attributs suivants :

**name**

* nom du paramètre à ajouter

**value**

* valeur du paramètre à ajouter

**Exemple :**

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:removeParam> {#cq-removeparam}

La balise `<cq:removeParam>` supprime un paramètre de requête avec le nom et la valeur spécifiés de la balise [`<cq:requestURL>`](#amp-lt-cq-requesturl) englobante. Si aucune valeur n’est fournie, tous les paramètres portant le nom donné sont supprimés.

Il possède les attributs suivants :

**name**

* nom du paramètre à supprimer

Exemple :

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

## Bibliothèque de balises Sling {#sling-tag-library}

La bibliothèque de balises Sling contient des fonctions Sling utiles.

Lorsque vous utilisez la bibliothèque de balises Sling dans votre script, celui-ci doit commencer par le code suivant :

```xml
<%@ taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %>
```

>[!NOTE]
>
>Lorsque le fichier `/libs/foundation/global.jsp` est inclus dans le script, la bibliothèque de balises sling est automatiquement déclarée.

### &lt;sling:include> {#sling-include}

La balise `<sling:include>` inclut une ressource dans la page active.

Il possède les attributs suivants :

**flush**

* Valeur booléenne définissant s’il faut vider la sortie avant d’inclure la cible.

**ressource**

* Objet de ressource à inclure dans le traitement de la demande en cours. La ressource ou le chemin d’accès doit être spécifié. Si les deux sont spécifiés, la ressource est prioritaire.

**chemin**

* Chemin d’accès à l’objet de ressource à inclure dans le traitement de la requête en cours. Si ce chemin d’accès est relatif, il est ajouté au chemin d’accès de la ressource actuelle dont le script inclut la ressource donnée. La ressource ou le chemin d’accès doit être spécifié. Si les deux sont spécifiés, la ressource est prioritaire.

**resourceType**

* Type de ressource de la ressource à inclure. Si le type de ressource est défini, le chemin doit être le chemin exact vers un objet de ressource : dans ce cas, l’ajout de paramètres, de sélecteurs et d’extensions au chemin n’est pas pris en charge.
* Si la ressource à inclure est spécifiée avec l’attribut path qui ne peut pas être résolu en ressource, la balise peut créer un objet de ressource de synthèse en dehors du chemin et de ce type de ressource.

**replaceSelectors**

* Lors de la répartition, les sélecteurs sont remplacés par la valeur de cet attribut.

**addSelectors**

* Lors de la répartition, la valeur de cet attribut est ajoutée aux sélecteurs.

**replaceSuffix**

* Lors de la distribution, le suffixe est remplacé par la valeur de cet attribut.

>[!NOTE]
>
>La résolution de la ressource et du script qui sont inclus avec la balise `<sling:include>` est la même que pour une résolution d’URL sling normale. Par défaut, les sélecteurs, l’extension, etc. de la requête actuelle sont également utilisés pour le script inclus. Ils peuvent être modifiés par le biais des attributs de balise : par exemple, `replaceSelectors="foo.bar"` permet de remplacer les sélecteurs.

Exemples :

```xml
<div class="item"><sling:include path="<%= pathtoinclude %>"/></div>
```

```xml
<sling:include resource="<%= par %>"/>
```

```xml
<sling:include addSelectors="spool"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include replaceSelectors="content" />
```

### &lt;sling:defineObjects> {#sling-defineobjects}

La balise `<sling:defineObjects>` expose les objets de script suivants, utilisés régulièrement, qui peuvent être référencés par le développeur :

**slingRequest**

* Objet SlingHttpServletRequest, donnant accès aux informations d’en-tête de requête HTTP - étend la requête HttpServletRequest standard - et donne accès à des éléments spécifiques à Sling tels que les informations de ressource, de chemin et le sélecteur.

**slingResponse**

* Objet SlingHttpServletResponse , fournissant l’accès à la réponse HTTP créée par le serveur. Il s’agit du même que l’objet HttpServletResponse à partir duquel il s’étend.**requête**
* Objet de requête JSP standard qui est un objet HttpServletRequest pur.**response**
* Objet de réponse JSP standard qui est un objet HttpServletResponse pur.

**resourceResolver**

* Objet ResourceResolver actif. Il est identique à slingRequest.getResourceResolver()

.**sling**

* Objet SlingScriptHelper contenant des méthodes pratiques pour les scripts, principalement sling.include(&#39;/some/other/resource&#39;) pour inclure les réponses d’autres ressources dans cette réponse (par exemple, l’incorporation de fragments de code HTML d’en-tête) et sling.getService(foo.bar.Service.class) pour récupérer les services OSGi disponibles dans Sling (notation de classe en fonction du langage de script).

**ressource**

* l’objet Resource actuel à gérer, selon l’URL de la requête. Elle est identique à slingRequest.getResource().

**currentNode**

* Si la ressource actuelle pointe vers un nœud JCR (ce qui est généralement le cas dans Sling), cela donne un accès direct à l’objet Node . Sinon, cet objet n’est pas défini.

**log**

* Fournit un enregistreur SLF4J pour la journalisation dans le système de journaux Sling à partir de scripts, par exemple log.info(« Executing my script »).

* Il possède les attributs suivants :

**requestName**

**responseName**

**nodeName**

l **ogName resourceResolverName**

**slingName**

**Exemple :**

```xml
<%@page session="false" %><%
%><%@page import="com.day.cq.wcm.foundation.forms.ValidationHelper"%><%
%><%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %><%
%><sling:defineObjects/>
```

## Bibliothèque de balises JSTL {#jstl-tag-library}

La [ Bibliothèque de balises standard de pages JavaServer ](https://www.oracle.com/java/technologies/java-server-tag-library.html) contient de nombreuses balises standard particulièrement utiles. Les bibliothèques de balises principales, de formatage et de fonctions sont définies par le `/libs/foundation/global.jsp` , comme illustré dans le fragment de code suivant.

### Extrait de /libs/foundation/global.jsp {#extract-of-libs-foundation-global-jsp}

```xml
<%@taglib prefix="c" uri="https://java.sun.com/jsp/jstl/core" %>
<%@taglib prefix="fmt" uri="https://java.sun.com/jsp/jstl/fmt" %>
<%@taglib prefix="fn" uri="https://java.sun.com/jsp/jstl/functions" %>
```

Après avoir importé le fichier `/libs/foundation/global.jsp`, comme décrit précédemment, vous pouvez utiliser les préfixes `c`, `fmt` et `fn` pour accéder à ces bibliothèques de balises. La documentation officielle de la JSTL est disponible à l’adresse [Tutoriel Java™ EE 5 - Bibliothèque de balises standard de pages JavaServer](https://docs.oracle.com/javaee/5/tutorial/doc/bnakc.html).
