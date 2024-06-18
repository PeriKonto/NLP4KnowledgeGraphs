# NLP4KnowledgeGraphs
I utilized natural language processing to create Knowledge Graphs. To achieve this I gathered relevant textual data from PubMed sources. I used entity recognition, to identify entities, followed by relation extraction which determined the relationships between identified entities.
Methods:

# Data Collection: 
The first step is to collect data from various sources, typically using web scraping techniques. This involves extracting relevant information from websites or APIs. Data collection may involve retrieving text, metadata, and links. 

# Entity Extraction: 
Once the data is collected, the next step is to extract entities from the text. Entities can be people, organizations, locations, events, or any other relevant entity. Techniques such as named entity recognition (NER) or part-of-speech tagging (POS) are used to identify and extract entities from the text. 

# Relation Extraction: 
After extracting entities, the next step is to extract relations between these entities. Relations represent the connections or interactions between entities. This step involves identifying patterns or dependencies in the text to determine how entities are related to each other. Dependency parsing and rule-based matching are common techniques used for relation extraction. 

# Knowledge Graph Construction: 
With entities and relations extracted, the knowledge graph is constructed. A knowledge graph is a graph-based data structure where entities are represented as nodes, and relations are represented as edges connecting these nodes. The extracted entities and relations are used to populate the nodes and edges of the graph.

Accordingly, I built a graph structure where entities are nodes and relationships are edges, viewed as a two-step approach:
# Step 1: 
Splited the text document or article into sentences and resolve coreferences using SpaCy pipeline. The sentences are then annotated to identify subjects and objects. (Knowledge graphs are constructed using parts-of-speech and dependency parsing techniques, allowing for scalable extraction of entity pairs from grammatical patterns found in large amounts of text, such as abstracts, leveraging NLP libraries).

# Step 2: 
Defined entity pairs as entities or noun chunks with subject-object dependencies connected by a root verb. Other approaches, such as subject-predicate-object triples, can be used to establish different types of connections. Single-word entities are identified using parts-of-speech (POS) tags, with nouns and proper nouns considered as entities. In cases where an entity spans multiple words, the dependency tree of the sentence is parsed to create relationships (edges) between nodes (subject and object) based on the sentence's grammar. 
