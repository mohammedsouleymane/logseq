- google summary
	- Here is an in-depth summary of each lecture based on the provided sources:
	- ### Lecture 1: Introduction
	  A core concept introduced is the definition of visualization (Vis): it is an augmentation of human capabilities, where computer-based visualization systems provide visual representations of datasets to help people carry out tasks more effectively. The "what-why-how" question is presented as a fundamental framework for vis design: "What data is shown?", "Why is the visualisation tool used (task)?", and "How is the vis idiom constructed in terms of design choices?".
	  
	  Visualization leverages the human visual system's "superpowers" due to its high-bandwidth channel, allowing for faster and more reliable visual reasoning than mental reasoning. It acts as an external representation or "external cognition" to augment human capacity, summarizing information without losing details ("details on demand"). Visualization supports human-in-the-loop exploration for scientific discovery (data analysis) and communication (presentation of existing knowledge). It is particularly useful for large datasets that dynamically change over time.
	  
	  The lecture highlights the importance of showing dataset details rather than just summaries, referencing Anscombe's Quartet as an example where statistical summaries hide the true structure of data. Interactivity is deemed necessary for visualization tools to handle complexity, allowing users to change the level of detail, show different aspects, or view different representations of data.
	  
	  Challenges in design are also discussed, emphasizing that most design possibilities will be ineffective. A good design must match the human perceptual and cognitive system and align with the intended task. The information visualization process involves data representation, data presentation, and interaction, with mapping between data and its visual form, and consideration of perception and visual thinking.
	  
	  The course includes an assignment involving the realization of an interactive information visualization for a chosen domain and dataset, typically a group project for four students, contributing 40% to the final grade. The final exam is an oral exam in English, covering lecture and exercise content, and counts for 60% of the overall grade, with specific time allocated for assignment questions and course content questions. Both the oral exam and the assignment must have a grade of 8/20 or higher to pass the course.
	- ### Lecture 2: Human Perception and Colour Theory
	  
	  This lecture delves into the principles of human perception and colour theory, crucial for designing effective visualizations. The core general guideline is to design graphic representations that enable quick perception of important data elements and patterns by considering human sensory capabilities. More important data should be represented by more visually distinct graphical elements, and greater numerical quantities by more distinct elements.
	  
	  The lecture outlines a three-stage model of visual perceptual processing:
	- **Stage 1: Parallel processing to extract low-level features** such as orientation, colour, texture, and motion, resulting in feature maps.
	- **Stage 2: Pattern perception** involving slower serial processing to identify continuous contours or regions of similar colour/texture, linked to the "Action" and "What" visual systems.
	- **Stage 3: Visual working memory**, which can hold only a few objects and provides answers to visual queries through cognitive processing. Attention influences all three stages.
	  
	  The anatomy of the human eye is detailed, including the variable focus lens, pupil, and retina. The retina contains rods (highly sensitive at low light levels) and cones (three distinct colour receptors: S-cones, M-cones, L-cones, supporting trichromacy). The brain constructs what we see, not just the retinal image. Concepts like focal length, depth of focus, visual field, and optimal screen settings (high-resolution display with moderate viewing angle) are discussed, emphasizing visual acuity for maximum data density.
	  
	  Brightness is explained as a dimension in colour space, with light receptors measuring relative light changes, making the eye a "change meter" rather than a "light meter". Various brightness illusions are presented, such as the Herman grid, simultaneous brightness contrast, and Chevreul illusion, which arise from the eye's edge-enhancing processing due to lateral inhibition. These contrast effects can lead to significant errors (up to 20%) in quantitative information presented in grayscale. A key guideline is to avoid using grayscale for more than a few numerical values. Shading algorithms in computer graphics (uniform/flat, Gouraud, Phong) are discussed in relation to these illusions. Guidelines for highlighting via luminance contrast and crispening are also provided.
	  
	  Colour blindness, affecting about 10% of males and 1% of females, is primarily due to a lack of L-cones (protanopia) or M-cones (deuteranopia), leading to difficulty distinguishing red and green. The lecture touches upon colour measurement (C=rR+gG+bB) and different colour spaces like sRGB and RGB.
	  
	  Practical guidelines for colour use include:
	- Using more saturated colours for small symbols or thin lines and less saturated colours for large areas.
	- Ensuring luminance contrast when displaying small symbols or text on a differently coloured background.
	- Using thin border lines with large luminance differences to define shapes when large areas use nearly equiluminous colours.
	- Using low-saturation, light, pastel colours for large background areas and high-saturation symbols for the foreground when layering.
	  Tools like ColorBrewer 2.0 and Viz Palette are mentioned as resources for colour advice.
	  
	  The lecture concludes with the importance of understanding visual perception for effective information visualization design.
	- ### Lecture 3: Data Representation
	  
	  This lecture focuses on "Data Representation," delving into the "what" part of the what-why-how analysis framework, providing a language for effective visualization design. Data is typically described using domain-specific language and must be translated into abstract structures to find suitable visual representations. Data abstraction helps narrow down the vast design space.
	  
	  The lecture distinguishes between semantics (real-world meaning) and types (data and datasets), noting that both drive aspects of vis design.
	  
	  **Data Types** are defined as fundamental building blocks:
	- **Item:** An individual discrete entity, like a table row or network node.
	- **Attribute:** A property that can be measured, observed, or logged, also called a variable or dimension, e.g., price or temperature.
	- **Link:** A relationship between items, such as between nodes in a network.
	- **Position:** Spatial data, like a location in 2D or 3D space.
	- **Grids:** Sampling continuous data based on geometric and topological relationships between cells.
	  
	  **Dataset Types** are collections of these data types:
	- **Tables:** Collections of information, common types include:
		- **Flat table:** Rows as items, columns as attributes, cells as values.
		- **Multidimensional table:** Indexing cells via multiple keys.
	- **Networks (graphs):** Define relationships between nodes (items) via links, where both nodes and links can have attributes.
	- **Trees:** Hierarchical structures without cycles, where each child has one parent.
	- **Fields:** Each cell contains measurements from a continuous domain, with issues of sampling and interpolation.
		- **Spatial fields:** Sampling at spatial positions; if position is given, it's "scientific visualization" (scivis), unlike "information visualization" (infovis) where space is designer-chosen.
		- **Grid types:** Uniform, rectilinear, structured, and unstructured grids, differing in how geometry and topology are stored.
	- **Geometry:** Information about the shape of items with spatial positions (points, lines, surfaces, volumes), which may or may not have attributes.
	- **Other combinations:** Clusters (grouping by similarity), sets (unordered groups), lists/arrays (ordered groups), paths (ordered segments in a network), and compound networks (network with superimposed tree).
	  Dataset availability can be static (offline) or dynamic (stream), with dynamic streams adding complexity.
	  
	  **Attribute Types** describe the nature of attributes:
	- **Categorical (nominal):** No implicit ordering, but often hierarchical or externally ordered (e.g., fruit types).
	- **Ordered:**
		- **Ordinal:** Well-defined ordering but no arithmetic (e.g., t-shirt size).
		- **Quantitative:** Measurement of magnitude supporting arithmetic comparison (integers, real numbers; e.g., height).
	- **Ordering directions:** Sequential (min to max), diverging (e.g., valleys/mountains), and cyclic (values wrap around, e.g., time).
	- **Hierarchical attributes:** Hierarchical structures within or between attributes (e.g., time series aggregated by day, week, month, year).
	  
	  **Key Versus Value Semantics** distinguish attributes based on their role:
	- A **key attribute** (independent) acts as an index to look up **value attributes** (dependent).
	- Keys can be categorical or ordinal; values can be any type.
	- In flat tables, keys can be implicit (row index) or explicit; multidimensional tables require multiple keys.
	- For fields, keys are independent variables to look up dependent values, leading to multivariate structures (scalar, vector, tensor fields) and multidimensional structures (e.g., 2D/3D fields).
	  **Temporal Semantics** are specifically addressed, noting the complexity of time data due to its multiscale hierarchy and aggregation challenges.
	  
	  The lecture transitions to **Task Abstraction**, the "why" part of the framework, which involves transforming domain-specific task descriptions into abstract forms to reason about similarities. User goals are categorized into three levels of abstraction:
	- **Analyse:** The most common use case for visualization, involving either **Consume** (finding new knowledge through **Discover/Explore**, presenting existing knowledge through **Present/Explain**, or casual enjoyment) or **Produce** (generating new material through **Annotate**, **Record**, or **Derive** new data elements).
	- **Search:** Involves knowing or not knowing the target and location: **Lookup** (known target, known location), **Locate** (known target, unknown location), **Browse** (unknown target, known location to look), **Explore** (unknown target, unknown location).
	- **Query:** After finding targets, perform operations to **Identify** their characteristics, **Compare** multiple targets, or **Summarise** all targets.
	  
	  Finally, the lecture mentions different **Targets** that users might be looking for in data: trends, outliers, features, single attributes, multiple attributes (dependencies, correlations, similarities), network topology, specific paths, and geometric shapes.
	- ### Lecture 4: Analysis and Validation
	  
	  Lecture 4 focuses on "Analysis and Validation" in information visualization design, particularly emphasizing the **Four Nested Levels of Vis Design** as outlined by T. Munzner. This framework suggests that design proceeds top-down from abstract concerns to concrete implementation, but validation must occur at each level:
	- **Domain Situation:** Understanding the target users, their domain of interest, data, and questions (tasks). The outcome is understanding user needs, often through observations or interviews. Challenges include users' inability to clearly specify needs and designers making assumptions.
	- **Data & Task Abstraction:** Translating domain-specific questions into generic representations (e.g., browsing, comparing, summarizing) and abstracting data into types suitable for visual representation.
	- **Visual Encoding & Interaction Idiom:** Designing specific ways to create and manipulate visual representations (visual encoding idiom) and how users change what they see (interaction idiom). This level has a large design space, which data and task abstractions help reduce, with choices based on human perception and memory.
	- **Algorithm:** Implementing the visual encoding and interaction idioms, considering factors like computational complexity, memory usage, and match with the idiom.
	  
	  The lecture stresses that most designs in the huge visualization design space are ineffective, making validation crucial from the beginning. Errors at upstream levels propagate downstream, necessitating an iterative design process. Each design level has its own **threats to validity**, such as choosing the wrong problem, abstraction, idiom, or algorithm.
	  
	  Various **Validation Approaches** are discussed:
	- **Immediate vs. Downstream Validation:** Immediate validation checks a specific design choice, while downstream validation assesses the impact of a choice on subsequent levels. Mismatches can occur if validation methods don't align with the claimed benefits (e.g., algorithm performance doesn't validate a visual encoding idiom).
	- **Domain Validation:** Aims to confirm real user needs are addressed. Methods include field studies (observing users in real-world settings) and semi-structured interviews (e.g., contextual inquiry). Downstream validation can involve observing a solution's adoption rate.
	- **Abstraction Validation:** Checks if identified task and data abstractions solve the target audience's problems. Downstream methods include qualitative feedback from target users and field studies to observe behavioral changes.
	- **Idiom Validation:** Justifies the idiom's design based on perceptual and cognitive principles. Methods include heuristic evaluation or expert reviews to prevent guideline violations. Downstream validation can use controlled experiments in lab settings (measuring time and errors), qualitative discussion of results (showing images/videos), quantitative quality metrics (e.g., edge crossings for graphs), and usability studies.
	- **Algorithm Validation:** Analyzes computational aspects like complexity, execution time, memory consumption, and scalability. It also verifies the correctness of the algorithm against the idiom specification. Standard benchmarks can be used for comparison.
	  
	  The lecture provides examples of case studies (MatrixExplorer, Genealogical Graphs, Flow Maps, LiveRAC, Sizing the Horizon) to illustrate how these validation methods are applied in practice.
	- ### Lecture 5: Data Presentation
	  
	  Lecture 5, "Data Presentation," focuses on how to visually encode data, building upon the previous discussion of data types. The core concepts are **Marks** and **Channels**.
	- **Marks:** These are the basic graphical elements or geometric primitives used to represent items or links in a visualization. They are classified by their spatial dimensions: zero-dimensional (points), one-dimensional (lines), or two-dimensional (areas). Three-dimensional marks (volumes) are less common due to perceptual limitations.
		- **Mark Types:**
			- **Item marks:** Represent individual data items (e.g., points for cities).
			- **Link marks:** Represent relationships between items:
				- **Connection marks:** Pairwise relationships via lines (e.g., lines connecting nodes in a network).
				- **Containment marks:** Hierarchical relationships using areas (e.g., nested rectangles in a treemap).
	- **Channels:** These control the appearance of marks and can be applied independently of the mark's dimensionality. Many visual channels exist: spatial position, shape, colour (hue, saturation, luminance), motion (flicker, direction, velocity), size (length, area, volume), and tilt (angle). Note that size and shape channels may not be applicable to all mark types (e.g., area marks are typically not size or shape coded).
		- **Channel Types:**
			- **Identity channels:** Convey what something *is* (e.g., shape, hue, motion pattern).
			- **Magnitude channels:** Convey *how much* of something there is (e.g., size, luminance, saturation, angle).
			  
			  The lecture emphasizes that the use of marks and channels is guided by two key principles:
	- **Expressiveness Principle:** A visual encoding should express *all* and *only* the information in the dataset attributes. Ordered data should be shown using magnitude channels; unordered (categorical) data should use identity channels to avoid implying non-existent ordering.
	- **Effectiveness Principle:** The importance of an attribute should match the salience (impact) of the channel used to encode it. The choice of which attributes to encode with spatial position is the most central, as position dominates a user's mental model.
	  
	  **Channel Effectiveness** is quantified by several factors:
	- **Accuracy:** How closely human perceptual judgment matches objective measurements (e.g., Steven's Psychophysical Power Law, which describes how sensory experience relates to physical intensity). Position along a common scale is the most accurate channel, while volume is quite inaccurate.
	- **Discriminability:** The number of distinguishable steps or "bins" available within a channel. Channels like line width have limited bins; the number of data values should not exceed available bins.
	- **Separability:** How independent channels are from each other. Fully separable channels allow clear encoding of different information, while integral channels (e.g., saturation and hue for small regions) lead to interference.
	- **Popout (Preattentive Processing):** The ability of a distinct item to stand out immediately from others, indicating massively parallel processing of low-level features. Channels like colour hue, tilt, size, shape, and proximity can cause popout. Popout is typically effective for a single channel at a time.
	- **Grouping:** How channels facilitate the perception of items as a group. Containment is the strongest cue, followed by connection, proximity, and similarity (hue, motion, shape).
	  
	  Other perceptual considerations include:
	- **Relative vs. Absolute Judgements:** The perceptual system is based on relative judgments (Weber's Law), meaning position along a scale is perceived more accurately than pure length judgments. Luminance perception is contextual, based on contrast.
	- **Colour (Hue) Perception:** Our visual system evolved for colour constancy, which can sometimes work against simple colour encodings. Luminance and saturation are magnitude channels, while hue is an identity channel.
	- **Colourmaps:** Define mappings between colours and data values, categorized as categorical or ordered (sequential, diverging). Guidelines include using magnitude channels (luminance, saturation) for ordered data, and specific hues for categorical data. Problems with rainbow colourmaps (hue indicating order, non-linear perception, poor fine detail) are highlighted, recommending monotonically increasing luminance colourmaps instead. Bivariate colourmaps are generally discouraged unless one attribute is binary. Colourblind-safe colourmaps are essential, avoiding red-green emphasis and using tools like Viz Palette.
	- **Size Channels:** Length is highly accurate, area is less accurate, and volume is quite inaccurate, suitable for ordered data.
	- **Tilt/Angle Channel:** Encodes magnitude based on mark orientation, with higher accuracy near horizontal, vertical, or diagonal positions.
	- **Shape Channel:** Applied to points and lines, can distinguish many bins but interacts strongly with size.
	- **Motion Channels:** Direction, velocity, flicker, and blinking frequencies are very separable and strongly draw attention, requiring careful use.
	- **Texture and Stippling:** Can convey categorical or ordered attributes through dimensions like orientation, scale, and contrast.
	- ### Lecture 6: Data Processing and Visualisation Toolkits
	  
	  Lecture 6, "Data Processing and Visualisation Frameworks," explores the tools and libraries available for creating visual representations of datasets. These frameworks support diverse purposes, including interactive data exploration, presentations, dashboards, business intelligence, and interactive storytelling.
	  
	  The lecture covers several prominent programming languages and their associated visualization libraries:
	- **R:** A free open-source programming language and environment primarily for statistical computing and graphics. It boasts effective data handling, operators for array/matrix calculations, and a large collection of data analysis packages. **ggplot2** is highlighted as a data visualization package for R, implementing Leland Wilkinson's Grammar of Graphics. **RStudio IDE** provides integrated tools like syntax highlighting, code completion, and a workspace browser for enhanced productivity.
	- **Dash:** An interactive visualization library that works with both R and Python. It combines Plotly graphing with a UI framework, using Flask for the backend (Python) and React.js for the frontend, and supports streaming data.
	- **D3.js (Data-Driven Documents):** A flexible JavaScript library that combines powerful visualization components with a data-driven approach to DOM manipulation. It's based on web standards (HTML5, SVG, CSS), allowing data to be bound to document elements for transformation based on visual properties. D3.js is very powerful and customizable due to its low-level API, but has a steep learning curve. It builds on earlier academic projects like prefuse, Flare, and Protovis. Libraries like NVD3, plotly.js, or Plotly's Chart Studio offer higher-level interfaces for non-programmers.
	- **React-Vis:** A React.js visualization library maintained by Uber, which is open-source and facilitates visualization creation using HTML tags rather than direct JavaScript DOM manipulation.
	- **Python:** A versatile language used with several libraries for data processing and visualization:
		- **NumPy:** Fundamental package for scientific computing.
		- **pandas:** A data analysis and manipulation tool.
		- **Matplotlib:** A library for creating static, animated, and interactive visualizations, with its Pyplot module offering a MATLAB-like interface.
		- **Seaborn:** A data visualization library with a high-level interface built on Matplotlib.
		- **Altair:** Enables declarative visualizations in Python.
	- **Bokeh:** An interactive visualization library for Python that allows export to HTML (for custom CSS/HTML), features widgets for interactive controls, and supports tooltips for data access, including streaming data via WebSockets.
	- **Streamlit:** Another interactive visualization library for Python, known for easy formatting with markdown and rapid prototyping. It supports Matplotlib, Seaborn, and Altair visualizations and also handles streaming data via WebSockets.
	  
	  Beyond programming libraries, the lecture introduces specialized visualization tools and platforms:
	- **Leaflet:** A JavaScript library specifically for interactive tiled maps, supporting data layers (SVG) on top of map tiles and smooth interaction across devices.
	- **Deck.gl:** A large-scale open-source WebGL-powered data visualization framework from Uber's Vis.gl, focusing on 3D map visualizations with support for streaming data and cartographic projections.
	- **Tableau:** A business intelligence tool for visual data analysis, known for creating interactive dashboards and handling huge, fast-changing datasets with integrations to various file types and database solutions (e.g., Hadoop, Amazon AWS, MySQL, SAP).
	- **Microsoft Power BI:** A business analysis tool providing interactive visualizations and business intelligence capabilities, enabling end users to create reports and dashboards. It connects to hundreds of data sources, including cloud-based BI services, and simplifies data preparation and analysis.
	- **Google Charts:** A free data visualization tool for creating interactive charts embeddable on websites, producing pure HTML5 and SVG output, and integrating dynamic data sources with Google dashboards and controls.
	- **Datawrapper:** Offers a simple interface for uploading data and creating embeddable visualizations, originally for journalists, enabling end-user authoring without programming skills and supporting PDF export.
	- **Infogram:** A web-based drag-and-drop platform for data visualization and infographics, allowing non-designers to create effective visualizations with a WYSIWYG editor and numerous chart types.
	  
	  The lecture concludes by mentioning other solutions like Shiny, FusionCharts, Grafana, Chartist.js, and ChartBlocks, indicating the vast landscape of visualization tools.
	- ### Lecture 7: Design Guidelines and Principles
	  
	  Lecture 7 covers essential "Design Guidelines and Principles" for information visualization, primarily based on Tamara Munzner's "Rules of Thumb". These guidelines aim to improve the effectiveness and usability of visualizations.
	- **No Unjustified 3D:**
		- 3D visualization is only justified for tasks involving shape understanding of inherently three-dimensional structures (e.g., spatial data like medical scans, fluid flows, molecular interactions), where benefits outweigh costs.
		- **Costs of 3D:**
			- **Power of the Plane:** Human perception is highly optimized for 2D, and importance on a plane is influenced by reading conventions.
			- **Disparity of Depth:** We perceive about 2.05D, not true 3D, with significantly less accuracy for depth (N=0.67 in Steven's Psychophysical Power Law) compared to 2D lengths (N=1.0). Stereo displays only slightly improve depth perception.
			- **Occlusion Hides Information:** The most powerful depth cue, occlusion, inherently hides parts of the data, requiring costly interactive navigation (motion parallax) and increased cognitive load to remember obscured information.
			- **Perspective Distortion Dangers:** Foreshortening makes objects appear smaller and shifts their position, distorting visual encoding of abstract data (e.g., making bar heights in a 3D bar chart harder to judge).
			- **Shadows and Shading:** Can add visual clutter and interfere with colour channels, with shadows potentially being mistaken for data marks.
			- **Tilted Text is Not Legible:** Text designed for 2D displays becomes blocky and less readable when tilted in 3D.
	- **No Unjustified 2D:**
		- Laying out data in 2D space must also be justified against simpler 1D lists. Lists can offer higher information density and are excellent for lookup tasks.
		- 2D layouts are beneficial when a task requires understanding the topological structure of a network, where showing relationships explicitly outweighs the spatial cost.
	- **Eyes Beat Memory:**
		- Comparing views simultaneously visible (side-by-side) imposes much lower cognitive load than relying on memorized previous views.
		- **Memory and Attention:** Short-term (working) memory and human attention have limited capacity, making conscious search difficult for many items.
		- **Animation vs. Side-by-Side Views:** While animation can be powerful for smooth transitions and context maintenance, it often imposes significant cognitive load, especially for complex changes.
		- **Change Blindness:** Users may fail to notice major changes if their attention is directed elsewhere, making complex multi-frame animations difficult to track.
	- **Resolution Over Immersion:**
		- There's a critical trade-off between pixel resolution and immersion (e.g., in virtual reality). The number of pixels is a major constraint in visualization design, and immersion rarely justifies the cost in resolution.
		- Immersive environments are often special-purpose and not integrated with typical computer-based workflows, hindering task switching. They might be helpful for specific shape understanding tasks like protein folding.
	- **Overview First, Zoom and Filter, Details on Demand:**
		- This is Ben Shneiderman's "Visual Information-Seeking Mantra".
		- **Overview:** Summarizes the dataset, showing all items simultaneously to help identify regions for further investigation, often presented at the start of exploration. Geometric zooming alone might be insufficient, requiring aggregation or semantic zooming.
		- **Zoom and Filter:** Allows users to reduce the data shown or change the level of detail.
		- **Details on Demand:** Specific details pop up in response to user selection, or detail views can be permanently visible alongside an overview.
	- **Responsiveness is Required:**
		- Users need immediate visual feedback (within one second) for actions, such as highlighting selections or drawing new frames during navigation.
		- For longer actions, a progress indicator should be shown.
		- Interaction design should consider latency (e.g., clicking vs. hovering for details) and different feedback mechanisms (fixed pane, popup, visual highlight). Interactivity also incurs human time and attention costs.
	- **Get it Right in Black and White:**
		- This guideline, by Maureen Stone, emphasizes designing critical aspects of the visualization to be legible even in black and white. It suggests using the luminance channel for the most important attributes.
	- **Function First, Form Next:**
		- Prioritize the function and effectiveness of the design over its aesthetic form. An effective but "ugly" design can be refined, but a beautiful, ineffective one cannot.
		- However, visual beauty does matter, as users prefer equally effective but more beautiful designs.
	- ### Lecture 8: Visualisation Techniques
	  
	  Lecture 8 delves into specific "Visualisation Techniques" for encoding different types of datasets: tables, spatial data, and networks/trees. It focuses on various "idioms" or ways information can be visualized.
	  
	  The choice of spatial arrangement is crucial because the use of space dominates a user's mental model and planar position offers the most effective channels for both ordered and categorical attributes.
	  
	  **1. Arrange Tables:**
	- **Keys and Values:** The distinction between key (independent index) and value (dependent data) attributes is central. Keys typically define spatial regions, while values are shown within them.
	- **Scatterplot (Bubble Plot):** Visually encodes two quantitative value attributes using horizontal and vertical spatial position for point marks. Additional attributes can be encoded with colour (categorical) or size (quantitative, forming a bubble plot). Useful for finding trends, outliers, distributions, and correlations.
	- **Separate, Order & Align Regions:** For categorical attributes, spatial regions are used to group similar items. This involves separating, ordering, and optionally aligning regions. A 1D list alignment is common, with values shown on a second dimension (e.g., bar charts).
	- **Bar Chart:** Encodes one quantitative value attribute and one categorical key attribute. Value is shown with aligned vertical position using line marks, and the key attribute separates marks horizontally. Ordering by data-driven attributes (e.g., weight) aids trend perception.
	- **Stacked Bar Chart:** For multidimensional tables with one quantitative value and two categorical keys. Sub-bars, length-coded and stacked vertically, encode the value for each category of the secondary key. Useful for part-to-whole relationships and trend finding.
	- **Streamgraph:** Visualizes time-series data (quantitative value, ordered time key, categorical key) emphasizing the continuity of horizontal layers. Layer height encodes counts, suitable for finding trends.
	- **Dot Chart:** Similar to a bar chart but uses point marks instead of lines for the quantitative attribute.
	- **Line Chart:** Best used for ordered key attributes to emphasize trends, as using it for categorical data implies non-existent trends (violates expressiveness). Aspect ratio can be "banked to 45°" for better angle judgment.
	- **Matrix Alignment:** For datasets with two keys, arranged in a 2D matrix.
		- **Heatmap:** Two categorical key attributes, one quantitative value attribute. Area marks in a 2D matrix alignment with a diverging colourmap, good for finding clusters, outliers, and summaries.
		- **Scatterplot Matrix (SPLOM):** Arranges scatterplots in a 2D matrix to show pairwise relationships between many attributes. Useful for finding correlation, trends, and outliers.
		- **Volumetric Grids & Recursive Subdivision:** For 3D fields; volumetric grids are generally not recommended for abstract data due to perceptual issues.
	- **Spatial Axis Orientation:**
		- **Rectilinear layouts:** Orthogonal horizontal and vertical axes.
		- **Parallel layouts:** Parallel coordinates visualize many quantitative attributes at once, showing trends, outliers, and correlations.
		- **Radial layouts:** Items distributed around a circle using angle, efficient for periodic patterns. Examples include radial bar charts (length coding, radial layout for periodic patterns), pie charts (area marks, angle channel for part-whole relationships, but less accurate than bar charts), and polar area charts (area marks, length channel, radial layout). Normalised stacked bar charts are also discussed for part-to-whole relationships.
	- **Spatial Layout Density:**
		- **Dense layout:** Uses small, packed marks for overview, sometimes single pixels, limiting channels to position and colour.
		- **Space-filling layout:** Fills all available space (e.g., treemaps), using area marks and containment, maximizing space for colour coding and labels, but eliminating white space.
		  
		  **2. Arrange Spatial Data:**
	- Primary importance is given to the provided spatial position as the layout substrate.
	- **Geometry:** Data derived from raw sources (e.g., geographic data) can be used as a backdrop, with cartographic data used to size-code marks (e.g., city population).
		- **Choropleth Map:** Uses given geographic geometry for area mark boundaries, with a sequential segmented colourmap for a quantitative attribute per region, useful for finding clusters.
	- **Spatial Fields:** Scalar fields (single value per cell, e.g., medical scans), vector fields (multiple values, e.g., fluid dynamics), and tensor fields (matrix per cell, e.g., stress).
		- **Isocontours:** Uses isolines to represent contours of scalar values, with close lines indicating rapid change.
		- **Topographic Terrain Maps:** Use derived isolines from 2D spatial fields to query shape.
		  
		  **3. Arrange Networks and Trees:**
	- Connections (links) can be represented by node-link diagrams, adjacency matrices, or enclosure.
	- **Node-Link Diagrams:** Use explicit connection marks, well-suited for understanding network topology (e.g., shortest paths, adjacent nodes). Examples include triangular vertical, spline radial, rectangular horizontal, and bubble tree layouts.
		- **Force-Directed Placement (SFDP):** Nodes are point marks, links are connection marks. Highly scalable for larger networks via multilevel algorithms, good for exploring topology and paths.
	- **Adjacency Matrix View:** Network nodes are laid out along horizontal and vertical edges of a square, with links indicated by coloured area marks at cell intersections. Offers better scalability, predictability, and stability than node-link diagrams, but is poor for understanding topological structure.
	- **Enclosure (Containment):** Uses containment marks (nesting) to show complete hierarchical structure, applicable only to trees, not general networks.
		- **Treemaps:** Use area marks and containment with a rectilinear layout to encode trees. Effective for querying attributes at leaf nodes and can scale to millions of nodes/links.
		- **GrouseFlocks:** A visualization for compound networks (tree superimposed on a network), showing network nodes as tree leaves.
	- ### Lecture 9: View Manipulation and Reduction
	  
	  Lecture 9 covers "View Manipulation and Reduction," which are critical interactive techniques for handling visual complexity in visualizations, especially with large datasets.
	  
	  **View Manipulation:** This involves changing a view over time to reduce complexity or visual clutter. Ways to manipulate a view include:
	- Selecting specific elements (items or attributes).
	- Reordering (sorting) items to find patterns based on different attributes.
	- Changing parameters of a specific idiom (e.g., mark sizes).
	- Semantic zooming.
	- Switching between different visualization idioms.
	- Examples include **LineUp** (slope graphs with reordering and animated transitions to compare rankings) and **Animated Transitions** (maintaining context between states).
	  
	  **Element Selection and Highlighting:**
	- **Element Selection:** Involves choosing which elements (data items, links, attributes, attribute levels) can be targets. This can be for single or multiple elements, and can distinguish between primary and secondary targets. Selection often defines the target for a subsequent action.
	- **Selection Highlighting:** Provides immediate visual feedback when elements are selected. This can be achieved by changing colour (hue, luminance, saturation for popout), adding/changing outlines, changing size, or using motion coding (e.g., slight movement) for data items. For link marks, colour, linewidth, or shape can be changed. Multiple highlighting choices can be combined, and selected items can be connected via explicit visual links (Context-preserving Visual Links).
	  
	  **Navigation: Changing Viewpoint:**
	- Navigation helps users explore large, complex datasets from different perspectives, often combining filtering and aggregation.
	- Key aspects of navigation are:
		- **Zooming:** Moving the virtual camera closer or further away from the image plane, changing the number of visible items and their detail level.
			- **Geometric Zooming:** Simply scales the view.
			- **Semantic Zooming:** In contrast, the fundamental appearance of objects changes based on the number of available pixels; details are added or removed, and different idioms might be used at different semantic zoom levels. Constrained navigation limits camera motion to prevent users from getting lost.
		- **Panning (translating):** Moving the camera parallel to the image plane (up/down, side-to-side).
		- **Rotating:** Spinning the camera around its axis (rarely used in 2D navigation).
		  
		  **Reduction:** This is a strategy for dealing with complexity by reducing the number of visible elements, either through filtering or aggregation. It's a bidirectional operation, allowing reduction or increase of elements.
	- **Reducing Attributes:** The number of attributes can be reduced in three ways:
		- **Slice:** A single attribute value defines which items are extracted (e.g., 3D to 2D reduction of spatial data).
		- **Cut:** A plane divides the viewing volume, hiding everything on one side.
		- **Project:** All items are shown, but specific attributes are omitted (often used with multiple views, e.g., 2D projections of a 3D scene).
	- **Filtering:** Eliminates elements based on attribute values, often through dynamic queries where users interactively choose ranges via UI widgets.
		- **Item filtering:** Reduces the number of items.
		- **Attribute filtering:** Keeps items but reduces the number of shown attributes.
		- A challenge is that users might forget about filtered elements ("out of sight, out of mind"). Examples include **FilmFinder** and **DOSFA** (Dimensional Ordering, Spacing and Filtering Approach) for document collections.
	- **Aggregation:** Combines many elements into a derived element (summary) rather than eliminating them. A challenge is that aggregation might hide interesting signals in the dataset (e.g., Anscombe's Quartet).
		- **Item aggregation:** Interactive aggregation/deaggregation of item sets.
		- **Attribute aggregation:** Grouping attributes by similarity or synthesizing new attributes based on averages; includes dimensionality reduction.
		- Examples: **Histograms** (aggregate quantitative values into bins), **Continuous Scatterplots** (aggregate overplot density), **Boxplot Charts** (show distribution spread/skew), and **Spatial Aggregation** (challenges with modifiable areal unit problem - MAUP).
		- **Dimensionality Reduction (DR):** Preserves meaningful structure using fewer attributes, assuming hidden structure/redundancy. Multidimensional Scaling (MDS) is a complex form of DR. Reduced data is often visualized as a scatterplot or SPLOM; only large clusters should be considered reliable.
	- ### Lecture 10: Interaction
	  
	  Lecture 10 emphasizes "Interaction" as a fundamental necessity for visualization tools, especially when dealing with complex data and display limitations. It outlines five major approaches for handling visual complexity: deriving new data, view manipulation, reduction (filtering/aggregation), **faceting into multiple views**, and **embedding (focus+context)**.
	  
	  **1. Facet Into Multiple Views:** This approach deals with complexity by dividing information across multiple views.
	- **Juxtapose Views Side by Side:** Views are placed next to each other, which can be enhanced by **coordination of views** to create **linked views**.
		- **Sharing of Encoding:** All channels are handled identically for an identical visual encoding. **Multiform views** have some aspects of visual encoding different between views, perhaps showing subsets of attributes to reduce clutter.
		- **Linked Highlighting (Brushing):** Interactively selected items in one view are highlighted with the same colour in all other linked views, revealing how a continuous region in one view distributes across others. The **Exploratory Data Visualizer** is given as an example.
		- **Sharing of Data:** Views can either show all the data (**shared data**) or a subset.
			- **Overview-detail (subset):** One view shows the entire dataset (overview), and another shows detailed information about a selected subset. This can involve subset data with shared encoding (e.g., bird's-eye map) or multiform views (e.g., details-on-demand).
			- **Small Multiples:** Multiple views with the same visual encoding but different partitions of the data, often aligned in a matrix to facilitate comparison.
		- **Partitioning into Views:** Data is divided between views based on attributes, typically categorical variables. This can use list or matrix alignment, or recursive subdivision. Examples include partitioning bar charts and Hierarchical Visual Expression (HiVE).
	- **Superimpose Views as Layers:** Multiple layers are placed on top of each other.
		- Design choices include the number of layers (often two: background/foreground), distinction of layers (non-overlapping visual channels), static vs. dynamic layers, and partitioning of items into layers.
		- Examples: **Cartographic Layering** (regions, roads, distinguished by colour saturation/luminance/size), **Superimposed Line Charts** (CPU utilization for machines, coloured by machine), and **Hierarchical Edge Bundles** (network and hierarchy layers with distinct colours).
		  
		  **2. Embed: Focus+Context:** This approach displays both detailed information (focus) and overview information (context) within a single view, aiming to avoid disorientation from navigation techniques like geometric zooming.
	- **Elide and Superimpose Data:** Some items are omitted or summarized (context), while focus items are shown in detail. Dynamic aggregation can be used for context, and superimposed layers can also create focus+context (e.g., **Toolglass and Magic Lenses**).
	- **Distortion:** Geometric distortion of contextual regions to provide more space for detail in the focus region. Design choices include number/shape/locality of foci and interaction metaphors (e.g., movable lenses). While good for topological network structures, distortion can severely impair length judgments and may not be immediately obvious to users.
		- Examples: **DOITrees** (multiple foci), **Fisheye Lens** (single, local radial focus, movable lens), **Hyperbolic Geometry** (single global radial focus by projecting from hyperbolic to Euclidean space), and **Nonlinear Magnification Fields** (multiple, local arbitrary regions). Graph exploration often combines techniques like fisheye lenses with highlighting.
	- ### Lecture 11: Dashboards
	  
	  Lecture 11 is dedicated to "Dashboards," defining them, identifying common design mistakes, and outlining strategies for effective design.
	  
	  A dashboard is formally defined as "a visual display of the most important information needed to achieve one or more objectives; consolidated and arranged on a single screen so the information can be monitored at a glance".
	  
	  Key characteristics of dashboards include:
	- **Visual Displays:** Combine text and graphics, with an emphasis on graphics for efficiency and richer meaning.
	- **Display Information for Objectives:** Offer access to a collection of information, often from diverse sources, typically focusing on Key Performance Indicators (KPIs).
	- **Fit on One Screen:** All information should be entirely visible "at a glance" without requiring scrolling or navigating multiple screens. Information might be refreshed in real time depending on objectives.
	- **Monitor Information at a Glance:** Information is presented as summaries or exceptions, with the main goal of showing what requires attention and a secondary goal of offering details for action.
	- **Small, Concise, Clear, and Intuitive Display Mechanisms:** Visualizations should not require much screen space, and the choice of technique (line charts, gauges, traffic signals) should be well-suited to the needs.
	- **Customized:** Displayed information must be tailored to specific individuals, groups, or functions.
	  
	  The lecture outlines **13 Common Mistakes in Dashboard Design** by Stephen Few:
	- **Exceeding the Boundaries of a Single Screen:** Fragmenting data across multiple screens or requiring scrolling hides information and reduces effectiveness.
	- **Supplying Inadequate Context for the Data:** Data presented without reference points (e.g., targets, comparisons) is meaningless.
	- **Displaying Excessive Detail or Precision:** Overly precise measures slow down interpretation without benefits.
	- **Choosing a Deficient Measure:** The measure chosen might be accurate but not the clearest way to communicate the intended message (e.g., using absolute values instead of percentages for deviations).
	- **Choosing Inappropriate Visualization Technique:** Using techniques poorly suited for the data or task (e.g., circles for unidimensional variables due to poor area comparison, pie charts for comparisons, or gratuitous spatial representations).
	- **Introducing Meaningless Variety:** Unnecessary diversity in visualization types forces perceptual shifts, wasting user time and effort.
	- **Using Poorly Designed Visualization Technique:** Issues like legends requiring excessive eye movement, inefficient ordering of elements, sensory overload from bright colours, lack of delimiters for numbers, or occluded text/needles. Emphasizes maximizing the "data-ink ratio" and avoiding "chart junk". Almost always avoid 3D graphs for business data due to occlusion.
	- **Encoding Quantitative Data Inaccurately:** Wrong axis scales or other design issues leading to misinterpretation.
	- **Arranging Data Poorly:** Lack of visual balance (e.g., placing important data in least prominent areas), unnecessary segmentation, or poor arrangement for comparisons (e.g., side-by-side instead of above-below for related items). Most important data must "pop out".
	- **Highlighting Important Data Ineffectively or Not at All:** Failing to direct the viewer's eyes to the most crucial information first.
	- **Cluttering Display with Useless Decoration:** Using logos, titles, background gradients, or unnecessary background maps that distract from the data.
	- **Misusing or Overusing Colour:** Excessive or inappropriate use of colour.
	- **Designing an Unattractive Visual Display:** An ugly dashboard discourages use; beauty should enhance data display without distracting from or obscuring it.
	  
	  Finally, the lecture provides **Strategies for Effective Dashboard Design**:
	- **Condensing Information with Summaries and Exceptions:** Representing large sets of numbers as single summaries (sums, averages) or highlighting critical values (exceptions) that require attention.
	- **Maximising the Data-Ink-Ratio:** Eliminating unnecessary "non-data ink" (decoration, banners, chart junk like grids, borders, 3D effects) and de-emphasizing remaining non-data ink (e.g., thin lines, muted controls). Conversely, enhancing "data ink" by highlighting the most important data (statically or dynamically).
	- **Designing Dashboards for Usability/UX:**
		- **Organize Information to Support its Meaning and Use:** Grouping by business functions, co-locating related items, delineating groups with minimal visual means (e.g., white space), supporting meaningful comparisons (combining items in single encoding, placing close, brushing/linking, comparative values, colour for grouping), and discouraging meaningless comparisons.
		- **Make the Viewing Experience Aesthetically Pleasing:** Choosing colours appropriately (minimal bright colours, less saturated/natural colours, pale background), and using legible fonts (decent size, no ornaments, different font for headings).
	- ### Lecture 12: Case Studies and Course Review
	  
	  Lecture 12 serves as a "Case Studies and Course Review," applying the "what-why-how" analysis framework and the four levels of validation to existing visualization systems. This helps students understand possibilities for designing new systems.
	  
	  The lecture analyzes four significant case studies:
	- **Scagnostics SPLOM (Scatterplot Matrix):**
		- A scalable idiom for exploring scatterplot matrices.
		- It uses **scagnostics** (scatterplot computer-guided diagnostics) which are nine measurements (monotonic, stringy, skinny, convex, striated, sparse, clumpy, skewed, outlying) that categorize the point distribution of scatterplots.
		- These measurements are then shown in a new "scagnostics SPLOM," which is effectively a "scatterplot of scatterplots," where each point represents an entire scatterplot from the original SPLOM.
		- It features **linked highlighting** between views, and selecting a point triggers a popup with the full scatterplot.
		- **What (Data):** Table; **What (Derived):** Nine quantitative attributes per scatterplot (pairwise combinations of original attributes).
		- **Why (Tasks):** Identify, compare, and summarize distributions and correlation.
		- **How (Encode):** Scatterplot, scatterplot matrix; **How (Manipulate):** Select; **How (Facet):** Juxtaposed small-multiple views coordinated with linked highlighting, popup detail view.
		- **Scale:** Original attributes: dozens.
	- **Hierarchical Clustering Explorer (HCE):**
		- Designed for systematic exploration of multidimensional tables, originally for genomics (genes vs. experimental conditions, with gene activity as quantitative value).
		- It derives a **cluster hierarchy** of items based on similarity measures.
		- Scalability targets were high (100-20,000 genes, 2-80 experimental conditions).
		- Scalability is achieved through a combination of visual encoding and interaction idioms.
		- **What (Derived):** Hierarchical clustering of table rows and columns (for cluster heatmap); quantitative derived attributes for each original attribute and pairwise combination; quantitative derived attribute for ranking criteria.
		- **Why (Tasks):** Find correlation between attributes; find clusters, gaps, outliers, trends within items.
		- **How (Encode):** Cluster heatmap, scatterplots, histograms; **How (Reduce):** Dynamic filtering, dynamic aggregation; **How (Manipulate):** Navigate with pan/scroll; **How (Facet):** Multiform views with linked highlighting and shared spatial position; overview-detail with selection in overview populating detail view.
		- **Scale:** Genes: 20,000; Conditions: 80; Gene activity: 1,600,000.
	- **PivotGraph:**
		- Encodes a **derived network** from an original network by aggregating groups of nodes and links into a "roll-up" based on categorical attribute values (up to two attributes).
		- Highly scalable, summarizing arbitrarily large numbers of nodes and links from the original network.
		- Visual complexity of the derived network depends on the number of attribute levels for the two roll-up attributes.
		- Complements standard network encoding idioms (node-link, matrix views) and can be used as a linked multiform view.
		- Well-suited for comparison across attributes at the aggregate level, but not for understanding topological network features.
		- **What (Data):** Network; **What (Derived):** Derived network of aggregate nodes and links by roll-up into two chosen attributes.
		- **Why (Task):** Cross-attribute comparison of node groups.
		- **How (Encode):** Nodes linked with connection marks, size; **How (Manipulate):** Change with animated transitions; **How (Reduce):** Aggregation, filtering.
		- **Scale:** Original network nodes/links: unlimited; Rollup attributes: 2; Levels per roll-up attribute: several, up to one dozen.
	- **InterRing:**
		- Visual encoding and interaction idioms for tree exploration.
		- Uses a **space-filling radial layout** for encoding the hierarchy.
		- Features a **multifocus focus+context distortion approach** for interaction.
		- Employs structure-based colouring (redundant) which is useful for coordination with other views.
		- Works well in combination with other views, supporting selection, navigation, roll-up/drill-down, and direct editing of the hierarchy.
		- **What (Data):** Tree.
		- **Why (Task):** Selection, rollup/drilldown, hierarchy editing.
		- **How (Encode):** Radial, space-filling layout; colour by tree structure; **How (Facet):** Linked colouring and highlighting; **How (Reduce):** Embed: distort; multiple foci.
		- **Scale:** Nodes: hundreds (labelled), thousands (dense); Levels in tree: dozens.
		  
		  The lecture then provides a comprehensive **Course Summary** covering all previously discussed topics, reinforcing the key concepts from each lecture. This summary serves as a guide for understanding the scope of the final oral exam, which covers content from both lectures and exercise sessions, including any videos shown. Students are expected to understand basic concepts and be able to report on all aspects of their assignment. The course also mentions opportunities for MA and PhD theses in various related fields.
		  
		  <!--EndFragment-->
- ## Lecture 1
  collapsed:: true
	- Gapminder, hans rosling
		- Let the dataset change you mindset
		- animated presentation in space and time
	- MindXpres Data visualisation
		- interactive data visualisation
		- interactive source code visualisation
		- enhanced video player
	- Australia Bushfires
		- Not a satellite image
		- 3D visualisation of one month of data
			- data collected by Nasa
		- Information visualisation can be misused to deliver the wrong message
	- What is Visualisation (Vis)?
		- **Computer-based visualisation systems provide visual representations of datasets designed to help people carry out tasks more effectively**
		- Augmentation of human capabilities
		- A vis idiom is a distinct approach to creating and manipulation visual representations
			- find best design for a particular task
		- Resource limitations
			- computers: computational capacity and scalability
			- humans: perceptual and cognitive capacity
			- displays: number of pixels
				- information density (data-ink ratio) = amount of information vs unused space
	- Why use Visualisation? (HVES)
		- Human eyes have superpower
			- visual system provides very high-bandwidth channel
		- Visual reasoning is way faster and more reliable than mental reasoning
			- perceptual interferences based on spatial location etc.
		- External representation or "external cognition"
			- augment human capacity beyond internal cognition and memory
			- information can be organised by spatial location
		- Summarise information without losing details (details on demand)
	- Human in the loop
		- many analysis problems are ill specified
			- many possible questions to be asked
			- human-in-the-loop exploration making use of human pattern detection
			- augment human capabilities rather than replacing the human in the loop
		- exploratory analysis for scientific discovery (data analysis)
		- visualization tools for presentation (communication)
			- presenting existing knowledge
	- Computer in the loop
		- visualisations of large datasets that might dynamically change over time
	- Showing dataset details
		- exploring a dataset to find patterns
			- not possible if you only see a summary of the dataset
		- assessing the validity of a statistical model
			- does the model fit the data?
		- statistical characterisation (descriptive statistics) of a dataset loses information through summarisation
			- single summary often an oversimplication hiding the true structure of a dataset
			- anscombe's quartet ("Anscombe's quartet **comprises
			   four datasets that have nearly identical simple descriptive statistics,
			   yet have very different distributions and appear very different when 
			  graphed**" wiki)
	- **Interactivity is necessary for vis tools handling complexity**
		- limitation of people and displays make it **impossible to show a large dataset at once**
		- change level of details
		- show **different aspect** of a dataset
		- different **representation and summaries** of data
		- different **presentation** of data
	- Difficulties in design
		- main issue is that **vast majority of the possibilities** in the design space will be **ineffective for any specific usage context**
		- design might be a **poor match with human perceptual and cognitive system**
		- design might be a **bad match with the intended task**
		- **design alternatives**: consider multiple alternative and choose the best one!
	- Search space metaphor for vis design
	- What-Why-How Question
		- What data is shown
		- Why is the visualisation tool used (task)
		- How is the vis idiom constructed in terms of design choices
	- Information visualisation process
		- Data ->
		  logseq.order-list-type:: number
		- Data representation (mapping) ->
		  logseq.order-list-type:: number
		- Data pesentation ->
		  logseq.order-list-type:: number
		- perception and visual thinking ->
		  logseq.order-list-type:: number
		- interaction -> links back to 1 - 3
		  logseq.order-list-type:: number
- ## Lecture 2 (DATA)
  collapsed:: true
	- General guidelines
		- design graphic representations should take human sensory capabilities into account
		- important data should be represented by graphical elements that are more visually distinct
		- Greater numerical quantities should be represented by more distinct graphical elements
	- Model of visual perceptual processing
		- Stage 1: Parallel processing to extract low-level features
			- billion of neurons working in parallel
			- orientation, colour, texture and motion
			- results in a set of feature maps
		- State 2: pattern perception
			- slow serial processing
			- continuous contours, regions of same colour or texture
			- two-visual-system theory: "Action" system and "What" system
		- Stage 3: Visual working memory
			- only a few objects in visual working memory
			- may provide answers to visual query (cognitive processing)
		- Attention affects all three stages
	- Cost and benefits of Visualisation
		- Where two or more tools can perform that same tasks, choose the one that allows for the most valuable work to be done per unit time.
		- Consider adopting novel design solution only when the estimated payoff is substantially greater than the cost of learning to use them.
		- Unless the benefit of novelty outweighs the cost of inconsistency, adopt tools that are consistent with other commonly used tools.
	- Gibson's Ecological Optics
		- Extract properties of surfaces
			- colour, texture
		- Ambient optical array
			- spherical array of light arriving at a given point
		- Optical flow
			- dynamic ambient optical array (moving objects, moving viewpoint)
			- perception of motion patterns
	- Anatomy of the human eye
		- variable focus **lens**
		- **pupil**
		- **retina**
			- what we see != image on the retina
			- two types of cells
				- rods, highly sensitive at low light levels
				- cones, three distinct colour receptors
			- brain forms our sight
				- focal length
				- maximum sharpness
	- Focus
		- Focus = focus distance
		- Depth of focus
			- distance eye-object = 50 cm
				- focus lies between 43 and 60 cm
			- distance eye-object = 3m
				- focus lies between 1.5m and infinite
	- Optimal Screen
		- use a high-resolution display with a moderate viewing angle for data analysis. This applies both to individual data analysis when the screen can be on a desktop and close to the use to collaborative data analysis when the screen muse be larger and farther away.
	- visual acuity
		- eyesight = retinal focus + brain interpretation
		- extent to which we can perceive details
			- ability to identify black symbols on a white back-ground at a standardised distance when the size of the symbols is varied
		- Important for the maximum density of data on a screen
	- Brightness
		- colour space can be divided into luminance (grey scale) and two chromatic (hue and saturation) dimension
		- light receptors in the eye
			- do not measure the amount of light on the retina
			- measure relative light changes over time and over adjacent spots on the retina
			- eye is a change meter rather than a light meter
			- Luminance refers to the measured amount of light coming from some region of space
	- Brightness illusion
		- Retinal ganglion cell receives input from multiple receptors(receptive field)
		- Processing tries to enhance edges
			- lateral inhibition from neighbouring neurons
	- Simultaneous contrast and erros
		- Simultaneous contrast effects result in large errors for quantitative information in grey scale
		- avoid using grey scale as a method for representing more than a few (two to four) numerical values
	- Contrast effects and shading
		- computer graphics shading algorithms (UGP)
			- uniforms (flat) shading
				- chevreul illusion
			- Gouraud shading
				- mach banding
			- Phong shading
				- smooth change with no appreciable Mach banding
	- Edge enhancement
		- Consider using Cornsweet contours instead of simple lines to define convoluted bounded regions.
	- Highlighting via contrast
		- consider using adjustments in luminance contrast as a highlighting method. It can be applied by reducing the contrast of unimportant items or by locally adjusting the background to increase the luminance contrast of critical areas.
	- Contrast crispening
		- more subtle grey values can be distinguished at the point of crossover
		- it subtle grey-level gradation within the bounds of a small  object are important, create low-luminance contrast between the object and its background.
	- Monitor/projector setup
		- Ideally, when setting up a monitor for viewing data, a light neutral-coloured wall behind the screen should reflect an amount of light comparable to the level of light coming from the monitor. The wall facing the screen should be of low reflectance (mid- to dark grey) to reduce reflections from the monitor screen. Lights should be placed so that they do not reflect from the monitor screen.
		- When setting up a room for a projection system, ensure that minimal room light falls on the projector screen. This can be done by means of baffles to shield the screen from direct illumination. Low-reflectance (mid- to dark grey) walls are also desirable, as the walls will scatter light, some of which inevitably reaches the screen.
	- Colour Breaking Camouflage
		- apples and leaves
		- using red and green to distinguish the two instead of all grey
	- Cone cell sensitivity(SML)
		- Cone cells, located in the retina, are responsible for color vision and are ==most sensitive to bright light.
	- Colour Blindness
		- About 10% of the male population and about 1% of the female population have some form of colour vision deficiency
		- Most commonly a lack of either the L-cons (protanopia) or the M-cones (deuteranponia)
			- both of these result in an inability to distinguish red and green
	- Colour spaces
		- chromaticity coordinates
			- hue (h) and saturation (s)
			- luminance is treated separately
		- Different colours spaces defined by different triangles (3 primary colours)
			- sRGB
			- RGB
			- adobe RGB
		- hue = pure color (red, blue, green)
		- saturation = intensity of the colour
		- luminance = brightness
	- Saturation of small/large area
		- more saturated = small symbols, thin lines, or other small areas.
		- less saturated colours = large area
		- If using colour saturation to encode numerical quantity, use greater saturation to represent greater numerical quantities. Avoid using a saturation sequence to encode more than three values
	- Luminance contrast
		- When small symbols, text or detailed graphical representations of information are displayed using colour on a differently coloured background, always ensure luminance contrast with the background.
	- Form
		- If areas are defined using nearly equiluminous colours, consider using thin border lines with large luminance differences (from the colours of the areas) to help define the shapes.
	- Colour Contrast illusion
		- same colour but looks different because of the background colour
	- Colouring Maps
		- Use low-saturation colours to colour code large areas. Generally, light colours will be best because there is more room in colour space in the high-lightness region than in the low-lightness region.
		- When colours coding large background areas overlaid with small coloured symbols, consider using all low-saturation, high-value (pastel) colours for the background, together with high-saturation symbols on the foreground.
	- ColorBrewer 2.0: Colour Advice for Maps
	- Viz Palette: same concept as colorbrewser
	-
- ## Lecture 3 (DATA REPRESENTATION)
  collapsed:: true
	- Data representation and abstraction
		- Detailed look at the what part of the what-why-how question
		- Provide a language that is meaningful and useful for vis design
		- Data is typically describe with domain language
			- translate the data into more abstract structure to find suitable visual representations
		- Data abstraction helps to narrow down the design space
	- Semantics and types
		- Many aspects of vis design driven by the kind of data
			- semantics (real-world meaning) (name, age, size)
			- types (data as well as datasets) (numbers, string)
		- What do the following datasets represent?
			- Basil, 7, S, pear
	- Data types (IALPG)
		- Item
			- individual discrete entity (table row or network node)
		- Attribute
			- also referred to as variable or dimension
			- property that can be measured, observed or logged
			- e.g. price or temperature
		- Link
			- relationship between items
			- e.g. between items (node) in a network
		- Position
			- spatial data
			- e.g. location in two-dimensional or three-dimensional space
		- Grids
			- sampling continuous data in term of geometric and topological relationships between its cells
	- Dataset types
		- tables
			- items, attributes
		- network and trees
			- items, links, attributes
		- fields
			- grid, position, attributes,
		- geometry
			- items
			- positions
		- cluster, set, list
			- items
	- Dataset
		- collection of information to be analysed
		- made out of the five data types
		- complex combination of basic dataset types are common
	- Tables
		- flat table
			- row represents an item of data
			- column represents an attribute of the dataset
			- a cell contains the value for a given item attribute
		- multidimensional table
			- indexing into a cell via multiple keys
	- Networks and trees
		- Network (graph)
			- defines relationships between two or more nodes (items) via links
			- nodes can have associated attributes
			- links can have associated attributes
			- e.g. people and their friendships or gene interaction network
		- trees
			- hierarchical structure without cycles
			- each child node has one parent node
			- e.g. company organisation chart or biological tree of life
	- Fields
	  collapsed:: true
		- Field
			- each cell contains measurements or calculation from a continuous domain
			- continuous data brings along the issues of sampling and interpolation
		- spatial fields
			- sampling at spatial positions
			- e.g. medical scan of a human body or measurements in wind tunnel
			- if spatial position is given with dataset, we talk about scientific visualisation (scivis) (in contrast of information visualisation (inforvis) where the use of space is chosen by the designer)
		- Grid types
			- uniform grid: sampling at regular intervals without any need to store grid geometry or grid topology (connection of cells)
			- rectilinear grid: supports non-uniform sampling
				- efficient storage information with high complexity in some areas and low complexity in others (also store grid geometry)
			- structured grid: enables curvilinear shapes where the geometric location of each cell needs to be specified
			- unstructured grid: complete flexibility but grid geometry as well as grid topology has to be stored explicitly
	- Geometry
	  collapsed:: true
		- Information about the shape of items with spatial positions
			- points and one-dimensional lines or curves
			- two-dimensional surfaces or regions
			- three-dimensional surfaces volumes
		- Geometry datasets do not necessarily have attributes
			- e.g. contours derived from a spatial field or shapes generated from raw geographic data (e.g. boundaries of a forest)
			- shown alone or as backdrop for other data
	- Other combinations
	  collapsed:: true
		- Cluster: grouping items based on similarity of attributes
		- set: unordered group of items
		- List(array): ordered group of items
		- path: ordered set of segments formed by links connecting nodes in a network
		- compound network(multilevel network): network combined with superimposed tree (with all the nodes of the network as leaves)
	- Dataset availability
	  collapsed:: true
		- static file (offline)
			- entire dataset is available all at once
		- dynamic stream (online)
			- dataset information trickles in over time
			- addition, update or deletion of items
			- adds complexity to the vis process
				- no longer have all data at a given time
	- Attribute types
	  collapsed:: true
		- ![image.png](../assets/image_1750163733629_0.png)
		- categorial(nominal) attributes
			- no implicit ordering (often hierachical)
			- external ordering can be superimposed
			- e.g. different types of fruits
		- Ordered attributes
			- ordinal data (e.g. t-shirt size)
			- quantitative (e.g. height, temperature or stock price)
		- Ordering directions
			- sequential: range max to min (e.g. mountain heights)
			- diverging (e.g. valleys in the sea and mountains on land)
			- cyclic (e.g. time measurements like the hour of the day or the day of the week)
		- Hierarchical attributes
			- hierarchical structures within or between multiple attributes
			- e.g. time series of daily stock prices where time can be aggregated hierarchically (from days to weeks, months and years)
	- Key vs value semantics
	  collapsed:: true
		- type of an attribute does not tell us about its semantics
		- key attributes (independent attribute) represents an index that is used to look up value attributes (dependant attributes)
			- key attributes can be categorical or ordinal
			- value attributes can be categorical, ordinal or quantitative
		- Flat tables
			- key might be implicit (simply the index of the row) or explicit (attribute within table with unique values)
		- Multidimensional tables
			- multiple keys are required to look up an item
			- combination of all keys must be unique for each item
		- Fields
			- independent variable to look up dependent variable
			- multivariate structure
				- **depends on number of value attributes**
				- scalar field: 1 attr/cell
				- vector field: 2+ attr/cell
				- tensor field: many attr/ cell
			- multidimensional structure
				- **depends on number of keys**
				- e.g. 2D or 3D fields
	- Temporal semantics
	  collapsed:: true
		- temporal attribute is any kind of information that is related to time
		- data about time is complicated to handle
			- time hierarchy is deeply multiscale (from nanoseconds to hour, decades to millennia)
			- temporal scales do not all fit into a strict hierarchy (e.g. weeks do not cleanly fit into months)
			- transformation and aggregation become complex
		- Time-varying semantics
			- time is one of the keys attributes (opposed to being a value)
			- time-series dataset
				- ordered sequence of time-values pairs
	- Task abstraction
	  collapsed:: true
		- next we have to investigate the why part of the what-why-how analysis framework
			- what is the goal of using the vis?
		- Transforms task description from domain-specific language into abstract form
			- enables reasoning about similarities
		- Who has the goal?
			- designer of the vis or the end user?
	- Actions (ASQ)
		- User goals can be defined by actions at three levels
			- analyse
				- consume existing or also produce additional data
			- search
				- what kind of search is involved (are the target and location known)?
			- query
				- need to identify one target, compare some targets or summarise all of the targets.
	- Analyse
		- consume (discover -> present -> enjoy)
		- produce (annotate -> record -> derive)
		- most common use case for vis is to consume information that has already been generated
	- Consume (DPE)
	  collapsed:: true
		- Discover (Explore)
			- use vis to find new knowledge that was not previously known
			- serendipitous observation of unexpected data
			- may be motivated by theories, models or hypotheses
			- outcome is to **generate a new hypothesis or verify (or disconfirm) an existing hypothesis**
			- need for sophisticated interactive vis idioms since we do not know in advance what the user will need to see
			- note that the why the vis is being used does not dictate the how
		- Present (Explain)
			- communication of information, telling a story with data or guiding au audience through a series of cognitive operations
			- output of a discover session might be become input for a present session
		- Enjoy
			- a casual encounter with vis (not driven by need to verify or generate a hypothesis)
	- Produce(ARD)
	  collapsed:: true
	  generate new material which is often immediately used as input for a next instance
		- Annotate
			- graphical or textual annotations of existing visualisation elements (might be stored as a new attribute)
			- typically a manual user action
		- Record
			- save or capture visualisation elements
			- screenshots, bookmarks, parameter settings or interaction logs
			- e.g. graphical history with a snapshot of the output of each task
		- Derive
			- produce new data elements based on existing data elements
			- strong relationship between the form of the data (attribute and dataset types) and the vis idioms that are effective at presenting it
			- derived attributes can be used to extend the dataset
				- from quantitative to ordinal data (water temp -> cold, warm or hot)
				- adding lat and lng to city name (via lookup in separate DB)
				- arithmetic operation on existing attributes
	- Targets
		- All data (TOF)
			- Trends
				- high-level characterisation of a pattern in the data (increases, decreases, peaks, plateaus)
			- Outliers
				- data that does not fit well with the backdrop
			- Features
				- task-dependent structures of interest
		- Attributes (SM)
			- single attributes (individual values, min or max)
			- multiple attributes (dependencies, correlation and similarities)
		- Network data
			- network topology as well as specific paths
		- Spatial data
			- understanding and comparing geometric shapes
	- Search (LLBE)
	  collapsed:: true
	  ![image.png](../assets/image_1750165464479_0.png)
		- Lookup
		  user knows what they are looking for and where it is
		- locate
		  user knows what they are looking for but does not know where it is
		- Browse
		  user does not know exactly what they are looking for but has a location in mind where to look
		- Explore
		  **user does not know what they are looking for and where to search**, often beginning from an overview of everything
	- Query (ICS)
		- Identify
			- if the search returns **known targets (lookup or locate)** then identify return their **characteristics**
			- if the search **returns targets matching particular characteristics (browse or explore)** the identify returns **specific references**
		- Compare
		  comparing multiple targets, it is more difficult than identifying tasks and requires more complex vis idioms
		- Summarize (overview)
		  scope are all possible targets
- ## Lecture 4 (DATA representation)
  collapsed:: true
	- ![image.png](../assets/image_1750172662202_0.png)
	- Validation
		- Huge vis design space and most designs are ineffective
		- Validate choices right from the beginning of the design process
			- top-down design (problem-driven work)
				- start at top situation domain level
				- major challenge at data/task abstraction; mainly use existing idioms
			- bottom-up design (technique-driven work)
				- inveniton of new idioms or algorithms
		- Independently validate all four levels of the design
			- domain validation
			- abstraction validation (what and why)
			- idiom validation (how)
			- algorithm validation
	- Four nested levels of Vis design (DAIA)
	  ![image.png](../assets/image_1750172903593_0.png)
	  Output from upstream level is input to downstream level
		- errors from upstream levels propagate to downstream levels
		- highly iterative design problem
	- Domain Situation
		- A domain situation is defined by
			- target users
			- domain of interest of target users(each domain might have its own vocabulary)
			- data of target users
			- questions(tasks) of target users
		- Outcome of design process
			- understanding of user needs (user-centered design)
		- Challenges and risks
			- users can often not clearly specify their analysis needs
			- designers make assumptions (rather than engaging with users)
		- Data & Task Abstraction
			- Abstract from answers to domain-specific questions at upstream to a generic representation
				- questions from different domains situations can map to the same abstract vis task
					- e.g. browsing, comparing or summarising
				- Design abstract data
					- data from upstream is often transformed into something different
					- determine which data type supports a visual representation that address a user's problem
		- Visual Encoding & Interaction Idiom
			- Specific way (idiom) to create and manipulate the visual representation of abstract data
				- visual encoding idiom
					- create a "picture" out of the data (what do users see?)
				- interaction idiom
					- how do users change what they see?
			- Design space of the combination of visual encoding and interaction idioms is very large
				- data and task abstractions help to reduce the number of potential visual encoding and interaction idioms
				- decision about good or bad matches based on human abilities (visual perception and memory)
		- Algorithm
			- Implementation of visual encoding and interaction idioms
				- can design different algorithms to realise the same idiom
			- Various factors might impact the choice of a specific algorithm
				- computational complexity (performance)
				- memory usage
				- level of match with visual encoding idiom
			- Separate algorithm design (computational issues) from idiom design (human perception issues)
	- Threats to Validity
		- Each design level has their own threats to validity
			- wrong problem, wrong abstraction, wrong idiom or wrong algorithm
	- Validation approaches
		- Can perform an immediate or downstream validation
			- downstream dependencies add to the difficulty of validation
				- e.g. poor algorithm design may have a negative effect when validation an interaction technique
			- use of mock-ups for early downstream evaluation
		- Mismatches
			- mismatch between the level at which the benefit is claimed and the chosen validation methodology
				- e.g. benefit of new visual encoding idiom cannot be validated by measuring the performance of the algorithm used downstream
			- carefully select the subset of validation methods matching the levels of design where contributions are claimed
	- Domain validation
		- A field study can help to validate that we are going to address real user needs
			- **observe people in real-word settings**
			- interviews
		- Downstream validation can for example investigate a solution's adoption rate by the target audience
			- **see what target users do** (without bringing them into a lab)
	- Abstraction validation
		- identified task abstraction and data abstraction might not solve the target audience's problems
		- downstream validation includes testing the solution with members of the target audience
			- **qualitative feedback** whether the tool is **useful**
			- **field study to observe and document how the target audience** uses the tool in their **real-world workflow**
				- observe changes in behaviour rather than document existing work practices
	- Idiom validation
		- Justify the design of the idiom with respect to **known perceptual and cognitive principles**
		- Heuristic evaluation or expert revies may be used to ensure that **no known guidelines are violated**
		- Downstream validation
			- **lab study**
			- **presentation and qualitative discussion of results**
			- **quality metrics**
			- **usability studies**
	- Algorithm Validation
		- Analyse computation complexity of algorithms
		- Downstream validation
			- execution time
			- memory consumption
			- scalability
		- Correctness of algorithm
		- Standard benchmarks might help to compare algorithms
	- ![image.png](../assets/image_1750174303580_0.png)
	- ![image.png](../assets/image_1750174322588_0.png)
	- ![image.png](../assets/image_1750174343846_0.png)
	- ![image.png](../assets/image_1750174351765_0.png)
	-
- ## Lecture 5 (Data presentation)
  collapsed:: true
	- Marks and Channels
		- **Marks** are basic **graphical elements**(geometric primitives) to represent **items or links**
		- **Channels** control the **appearance of marks**
		- Vis design space described by orthogonal combination of marks and channels
		- complex visual encodings can be decomposed and analysed in terms of their marks and channels
	- Marks
	  ![image.png](../assets/image_1750174687910_0.png)
		- Basic geometric/graphical element in an image
		- Zero, one or two dimensional marks
			- three dimensional marks (volumes) are not used frequently due to limited perception
	- Mark types
		- **item marks**
		- **link marks**
			- **connection** marks (pairwise)
			- **containment** marks (enclosure or nesting)
	- Channels
	  ![image.png](../assets/image_1750174814274_0.png)
		- control appearance of mark independently of the dimensionality of the geometric primitive
		- Many visual channels
			- shape, spatial position, colour, motion, size, tilt
		- **Size and shape** channels cannot be used on all types of marks
			- e.g. area marks typically not size or shape coded
	- Channel types
		- identity channels
			- **information** about **what** something is
			- e.g. shape, hue channel, motion pattern
		- Magnitude channels
			- how much of something is there
			- e.g. size, luminance or saturation colour channels
	- Using marks and channels
		- Progression of chart types
		- In examples each attribute encoded vis single channel
			- multiple channels might also be used redundantly
		- Use of marks and channels guided by the **principles of expressiveness and effectiveness**
			- after identifying most important attributes ensure that they are encoded with the highest ranked channel
		- Expressiveness principle
			- visual encoding should express **all of, and only, the information in the dataset attributes**
				- ordered attr -> magnitude channels
				- unordered attr -> identity channels
		- Effectiveness principle
			- importance of attribute should match the salience(noticeable) of the channel
			- most important attributes encoded with most effective channel
		- Attributes encoded with position will dominate the user's mental model
			- choice of which attributes to encode with position is the most central choice in visual encoding
	- Channel effectiveness
		- quantify effectiveness via accuracy
			- how close is human perceptual judgement to some objective measurement of the stimulus?
		- Different visual channels are perceived with different levels of accuracy
			- characterised by steven's psychophysical power law
		- Channel effectiveness mainly based on accuracy but also takes into account (dspg)
			- discriminability
			- separability
			- popout
			- grouping
	- Steven's Psychophysical Power law : $S=I^N$
		- Responses to sensory experience of magnitude are characterisable by power laws
			- S = perceived sensation
			- I = physical intensity
			- exponent N depends on sensory modality
			- most stimuli are magnified (superlinear) or compressed (sublinear)
	- Error rates across channels
	  ![image.png](../assets/image_1750179591785_0.png)
	- Discriminability
		- Quantify the number of distinguishable steps (bins) that are available within a visual channel
			- some channels (e.g. line width) have a very limited number of bins
			- small number of bins is not a problem if the number of values to be encoded is also small
			- number of different values that need to be shown for an attribute must not be greater than the available bins for the visual channel
	- Separability
		- Channels are not always completely independent from each other (interchannel interference)
			- ranging from fully separable channels to the inseparably combined integral channels (major interference)
		- Visual encoding straightforward with separable channels
			- encoding of different information in integral channels will fail
	- Popout
		- many channels provide visual popout where a distinct item stands out from many others immediately
		- most pairs of channels do not support popout
			- use popout for a single channel at a time
		- popout channels
			- tilt, size, shape, proximity, shadow direction
	- Grouping
		- Containment (links) is the strongest cue for grouping following by connection coming in second
		- items sharing the same level of a categorical attribute can also be perceived as a group
		- proximity is the third strongest grouping approach
		- similarity (hue, motion and shape)
			- shape and motion channel to be used with care
	- Relative versus absolute judgements
		- perceptual system fundamentally based on relative judgements and not absolute ones (webers's Law)
			- e.g. position along a scale can be perceived more accurately than pure length judgement without a scale
		- Perception of luminance is contextual based on the contrast with surrounding colours
	- Colour (Hue) Perception
	  ![image.png](../assets/image_1750185491963_0.png)
		- Our visual system evolved to provide colour constancy
			- same surface identifiable across illumination conditions
			- visual system might work against simple colour encodings
	- Mapping colour
		- Luminance and saturation are magnitude channels while hue is an identity channel
			- luminance can be used for two to four levels(bins)
			- saturation can be used for up to three levels (bins)
				- strongly interacts with size channel
			- saturation and hue are non-separable channels for small regions
	- comparing HSL lightness
		- computed HSL lightnss L is the smae for all six colours
			- true luminance as measured by an instrument
			- perceived luminance L* represents what we see
				- more sensitive to certain wavelengths (green and yellow) as shown earlier with spectral sensitivity
	- No implicit order for Hue
		- Sometimes learned hue order (not at perception level)
			- green-yellow-red from traffics lights
			- rainbows colour ordering
	- Colourmaps
		- A colourmap defines a mapping between colours and data values
		- Colourmaps can be categorical or ordered (sequential or diverging)
			- use magnitude channels of luminance and saturation for ordered data
	- Categorical colourmaps
		- Categorical colourmaps (qualitative colourmaps) are normally segmented (not continuous)
			- effective for categorical data (next best channel after position)
		- good resource for creating colourmaps is colorbrewer
		- Can use six to twelve distinguishable hue steps (bins) for small separated regions
			- includes background colour and default object colours
			- use easy nameable colours: e.g. red, blue, green, yellow, orange, brown, pink, magenta and cyan
		- use highly saturated colours for small regions
		- use low-saturation colours (pastels) for large regions
	- Ordered colourmaps
		- sequential colourmap ranges from a min value to a max value
			- use luminance or saturation channel
		- diverging colourmap
			- use two hues at the endpoints and a neutral colour as a midpoint
	- Rainbow vs two-hue colour map
		- how many hues to use in continuous colourmaps?
			- high-level structure vs local neighbourhoods
			- rainbow colourmap makes it easier to discuss specific subranges
	- Rainbow continuous colourmaps
		- problems of rainbow continuous colourmaps
			- hue is used to indicate order despite being an identity channel
			- scale is not perceptually linear
			- fine details cannot be perceived via the hue channel
				- luminance better
			- the 3 problems of rainbow continuous colourmaps can be addressed by using monotonically increasing luminance colourmaps
				- multiple hues are ordered according to their luminance from lowest to highest
			- rainbow colourmap
			  ![image.png](../assets/image_1750186250344_0.png)
	- Bivariate colourmaps
		- safest use of colour channel is to visually encoe a single attribute (univariatie)
		- in the colourmap categorisation we have seen colour maps encoding two separate attribute (bivariate)
			- if one of the two attributes is binary then it is straightforward to create a comprehensible bivariate colour colourmap
				- choose base set of hues and vary the saturation
			- if both attributes are categorical with multiple levels the results will be poor
			- combinations of sequential and diverging attributes should be used carefully
				- appear frequently in vis solutions but some people have difficulties to interpret their meaning
	- Colourblind-safe colourmaps
		- A safe strategy is to avoid using the hue channel only
			- e.g. vary luminance or saturation in addition to hue in categorical colourmaps
		- Avoid colourmaps emphasising red-green
		- Use colour blindness simulators and tools such as Viz Palette
	- Size channels
		- Suitable for ordered data but interacts with most other channels
			- length (1D): judgment of length is very accurate
			- area (2D): judgement of area is less accurate
			- volume (3D): volume channel is quite inaccurate
	- Tilt/Angle channel
		- encode magnitude information based on the orientation of a mark
			- tilt: against global frame
			- angle: line with respect to another line
		- Accuracy of our perception of a tilt/angle is not uniform
			- very accurate near exact horizontal, vertical or diagonal positions
	- Other channels
		- Shape channel
			- commonly applied to point marks
			- can also be applied to line marks
		- Motion channels
			- direction of motion
			- velocity of motion
			- flicker and blinking frequency
			- very separable from all other static channels
		- Texture and stippling channel
			- texture can be simplified by considering it as a combination of the following 3 perceptual dimensions
				- orientation, scale and contrast
			- texture can be used to show categorical attributes as well as ordered attributes
			- stippling fills regions of drawing with short strokes (dashed or dotted lines)
- ## Lecture 9
  collapsed:: true
	- View manipulation
		- Why to manipulate and change the view?
			- dataset might be too large to show everything at once
				- reduce complexity of single view
			- single static view might lead to visual clutter
		- How to manipulate/change a view over time?
			- select specific elements (items or attributes)
			- reordering (sorting) of items
				- find pattern by ordering based on different attributes
				- change parameters of a particular idiom
					- range of possible mark sizes
			- semantic zooming
			- switch between idioms
	- Change between Visual encoding idioms
	- line up example with reordering
		- Slope graphs (bump charts) with connecting line marks linking the same items together
	- LineUp
		- What(Data) Table.
		- What(Derived) Ordered attribute: weighted combination of selected attributes.
		- Why(Task) Compare rankings, distributions.
		- How (Encode) Stacked bar charts, slope graphs.
		- How (Manipulate) Reorder, realign, animated transitions
	- Animated transitions example
		- maintain a sense of context between states
		- what: compound network
		- how: change with animated transition. Navigation between aggregation levels
	- Element Selection
		- Different design choices for element selection
			- Which element can be selection targets?
				- data items, links, data attributes, levels within a data attribute,....
			- one kind of selection vs. multiple kinds of selection (e.g. via hover)
				- multiple mouse buttons or combination  with key presses for more advanced types of selections
			- selection of single elements vs selection of many elements
			- selection of primary and secondary target
				- e.g. for path traversal from source to target in a direct graph
			- selection often defines the target of a next action
	- Selection Highlighing
		- provide immediate visual feedback to users about element selection
			- different possibilities for highlighting of data items
				- changing colour
				- outline
				- change size
				- slightly moving items/pattern
			- different possibilities for highlighting link mark
				- changing colour
				- change linewidth, shape
			- multiple highlighting design choices can be combined
			- selected items might be connect via explicit visual links (connection marks)
	- Context-preserving visual links
		- what: any data
		- how: any encoding, highlight with link mark
		- how: select any element
		- how: juxtaposed multiple views
-