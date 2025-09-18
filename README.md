# CustomerClusturing
This project applies clustering techniques (K-Means) to segment mall customers based on their **Annual Income** and **Spending Score**. The goal is to understand customer behavior and identify meaningful groups for marketing strategies.

This project applies Unsupervised Machine Learning techniques to segment customers into meaningful groups. The workflow is structured as follows:

🔹 1. Data Loading & Exploration

Imported dataset using pandas.read_csv().

Conducted initial exploration with head(), info(), and describe().

Checked distributions of key features such as Age, Annual Income, and Spending Score.

🔹 2. Data Preprocessing

Selected relevant features for clustering.

Applied StandardScaler() (from sklearn.preprocessing) to normalize values, ensuring features with different scales (e.g., income vs. age) contribute fairly to clustering.

🔹 3. Clustering Algorithm: K-Means

Implemented K-Means Clustering (sklearn.cluster.KMeans) to group customers.

Key methods:

.fit_predict() → trains the model and assigns each record to a cluster.

.cluster_centers_ → provides the centroids of each cluster.

🔹 4. Determining Optimal Number of Clusters

Used the Elbow Method:

Iterated over different values of k (number of clusters).

Computed Within-Cluster Sum of Squares (WCSS / inertia_).

Visualized results using matplotlib to select the optimal k.

🔹 5. Cluster Analysis

Univariate clustering: segmented customers by a single feature (e.g., income).

Bivariate clustering: segmented by two features (e.g., income vs. spending).

Multivariate clustering: extended analysis with three features (age, income, spending).

🔹 6. Visualization

Plotted clusters using matplotlib (plt.scatter, plt.figure) and seaborn (sns.scatterplot, sns.pairplot).

Added cluster centroids (marker='*') for clarity.

Saved key plots with plt.savefig() for reporting.

🔹 7. Results

Customers were successfully segmented into meaningful groups (e.g., high-income high-spending, low-income low-spending, etc.).

These clusters can be leveraged for targeted marketing, personalized promotions, and strategic decision-making.

⚡ Tools & Libraries Used:

pandas, numpy → data manipulation

matplotlib, seaborn → visualization

scikit-learn (KMeans, StandardScaler) → clustering & preprocessing
