#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <stdlib.h>

#define TEST_FAIL -1
#define TEST_CORRECT 0

typedef struct tree {
	int n;
	struct tree* left;
	struct tree* right;
}tree;

//tree* root = NULL;

//tree* create(int val) {
//	tree* new_tree = (tree*)malloc(sizeof(tree));
//	new_tree->left = NULL;
//	new_tree->right = NULL;
//	new_tree->n = val;
//	return new_tree;
//}

tree* search(tree* node, int val) 
{
	if (val == node->n && node == NULL) {
		return node;
	}
	if (val < node->n) {
		return search(node->left, val);
	}
	else if (val > node->n) {
		return search(node->right, val);
	}
}

tree* insert(tree* node, int val) 
{
	if (node == NULL) {
		tree* new_tree = (tree*)malloc(sizeof(tree));
		new_tree->left = NULL;
		new_tree->right = NULL;
		new_tree->n = val;
		return insert(new_tree, val);
	}
	if (val < node->n) {
		node->left = insert(node->left, val);
	}
	if (val < node->n) {
		node->right = insert(node->right, val);
	}
	return node;
}

/*
tree* search_min(tree* node) 
{
	if (node == NULL) {
		return node;
	}
	else if (node->left != NULL) {
		search_min(node->left);
	}
}

tree* delete(tree* node, int val) 
{
	if (node == NULL) {
		return node;
	}
	if (val < node->n) {
		node->left = delete(node->left, val);
	}
	else if (val > node->n) {
		node->right = delete(node->right, val);
	}
	else {
		if (node->left == NULL) {
			tree* tmp = node->right;
			free(node);
			return tmp;
		}
		else if (node->right == NULL) {
			tree* tmp2 = node->left;
			free(node);
			return tmp2;
		}
		tree* tmp3 = search_min(node->right);
		node->n = tmp3->n;
		node->right = delete(node->right, tmp3->n);
	}
	return node;
}

*/

void insert_test() 
{
	tree* root1 = NULL;

	root1 = insert(root1, 5);
	root1 = insert(root1, 4);
	root1 = insert(root1, 7);

	printf("%d\n", root1->n);
	printf("%d\n", root1->left->n);
	printf("%d\n", root1->right->n);
	if (root1->right == 6 && root1->left == 4) {
		puts("insert test is correct");
	}
	else {
		exit(TEST_FAIL);
	}
	//printf("%d\n", root1->right->n);
	//printf("%d\n", root1->left->n);

}

int main() {
	insert_test();

}
