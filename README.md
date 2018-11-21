

typedef struct node1{    // left는 data보다 작은 값을 가진 노드들 right는 더 큰 값의 노드들
	int data; 
	struct node1* left;
	struct node1* right;
}T_NODE;
typedef struct{
	int count;
	T_NODE* root;
}BST_TREE;

T_NODE* add_bst(T_NODE* root,int data){
-data 값을 이용하여 새로운 노드를 만든다.
-root의 값과 비교해서 리컬시브하게 삽입해준다.

T_NODE* find_smallest_node(T_NODE* root){
-리컬시브하게 루트의 값을 비교해주면서 left로 이동

T_NODE* find_largest_node(T_NODE* root){
-리컬시브하게 루트의 값을 비교해주면서 right로 이동

T_NODE* search_bst(T_NODE* root,int key)
-루트보다 작으면 left로 비교
-루트보다 크면 right로 비교

T_NODE* delete_bst(T_NODE* root,int data,bool* success){
-루트와 값을 비교하면서 삭제해야할 데이터를 찾는다.
-노드를 찾으면 left와 right가 있는지 확인하고 이에 따라 삭제를 진행한다.
-left와 right가 둘다 존재하면 left노드의 맨 오른쪽 아래 노드를 노드가 삭제된 위치로 옮겨주면 tree가 잘 유지된다.

void traverse_inorder(T_NODE* root){
-left,root,right순으로 데이터 출력

void traverse_postorder(T_NODE* root){
-left,right,root순으로 데이터 출력

void traverse_preorder(T_NODE* root){
-root,left,right순 으로 데이터 
