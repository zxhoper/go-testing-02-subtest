package sum

import "testing"

func TestInts(t *testing.T) {
	s := Ints(1, 2, 3, 4, 5)
	if s != 15 {
		t.Errorf("sum of one to five should be 15; got %v", s)
	}

	s = Ints()
	if s != 0 {
		t.Errorf("sum of no numbners should be 0; got %v", s)
	}

	s = Ints(1, -1)
	if s != 0 {
		t.Errorf("sum of one and minus one should be 0; got %v", s)
	}
}

// Use struct
func TestIntsUsingTableOfStruct(t *testing.T) {

	// tt => Table of Test case
	tt := []struct {
		numbers []int
		sum     int
	}{
		{[]int{1, 2, 3, 4, 5}, 15},
		{nil, 0},
		{[]int{1, -1}, 0},
	}

	// range Test Cases
	for _, tc := range tt {
		s := Ints(tc.numbers...)
		if s != tc.sum {
			t.Errorf("sum of %v should be %v; got %v", tc.numbers, tc.sum, s)
		}
	}

}

// Use struct with notes
func TestIntsUsingTableOfStructNote(t *testing.T) {

	// tt => Table of Test case
	tt := []struct {
		name    string
		numbers []int
		sum     int
	}{
		{"one to five", []int{1, 2, 3, 4, 5}, 15},
		{"no numbers", nil, 0},
		{"one and minus one", []int{1, -1}, 0},
	}

	// range Test Cases
	for _, tc := range tt {
		s := Ints(tc.numbers...)
		if s != tc.sum {
			t.Errorf("sum of %v should be %v; got %v", tc.numbers, tc.sum, s)
		}
	}

}

// Test a specific test
// bash$ go test -run Foo -v
func TestFoo(t *testing.T) {
	t.Fatalf("foo always fails")
}
